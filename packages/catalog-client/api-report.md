## API Report File for "@backstage/catalog-client"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Entity } from '@backstage/catalog-model';
import { EntityName } from '@backstage/catalog-model';
import { Location as Location_2 } from '@backstage/catalog-model';

// @public (undocumented)
export type AddLocationRequest = {
    type?: string;
    target: string;
    dryRun?: boolean;
    presence?: 'optional' | 'required';
};

// @public (undocumented)
export type AddLocationResponse = {
    location: Location_2;
    entities: Entity[];
};

// @public (undocumented)
export interface CatalogApi {
    // (undocumented)
    addLocation(location: AddLocationRequest, options?: CatalogRequestOptions): Promise<AddLocationResponse>;
    // (undocumented)
    getEntities(request?: CatalogEntitiesRequest, options?: CatalogRequestOptions): Promise<CatalogListResponse<Entity>>;
    // (undocumented)
    getEntityByName(name: EntityName, options?: CatalogRequestOptions): Promise<Entity | undefined>;
    // (undocumented)
    getLocationByEntity(entity: Entity, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    getLocationById(id: string, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    getOriginLocationByEntity(entity: Entity, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    removeEntityByUid(uid: string, options?: CatalogRequestOptions): Promise<void>;
    // (undocumented)
    removeLocationById(id: string, options?: CatalogRequestOptions): Promise<void>;
}

// @public (undocumented)
export class CatalogClient implements CatalogApi {
    constructor(options: {
        discoveryApi: DiscoveryApi;
    });
    // (undocumented)
    addLocation({ type, target, dryRun, presence }: AddLocationRequest, options?: CatalogRequestOptions): Promise<AddLocationResponse>;
    // (undocumented)
    getEntities(request?: CatalogEntitiesRequest, options?: CatalogRequestOptions): Promise<CatalogListResponse<Entity>>;
    // (undocumented)
    getEntityByName(compoundName: EntityName, options?: CatalogRequestOptions): Promise<Entity | undefined>;
    // (undocumented)
    getLocationByEntity(entity: Entity, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    getLocationById(id: string, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    getOriginLocationByEntity(entity: Entity, options?: CatalogRequestOptions): Promise<Location_2 | undefined>;
    // (undocumented)
    removeEntityByUid(uid: string, options?: CatalogRequestOptions): Promise<void>;
    // (undocumented)
    removeLocationById(id: string, options?: CatalogRequestOptions): Promise<void>;
    }

// @public (undocumented)
export type CatalogEntitiesRequest = {
    filter?: Record<string, string | string[]>[] | Record<string, string | string[]> | undefined;
    fields?: string[] | undefined;
};

// @public (undocumented)
export type CatalogListResponse<T> = {
    items: T[];
};


// (No @packageDocumentation comment for this package)

```
