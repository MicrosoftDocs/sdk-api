---
UID: NE:searchapi._CatalogStatus
title: CatalogStatus (searchapi.h)
description: Used by ISearchCatalogManager::GetCatalogStatus to determine the current state of the catalog.
helpviewer_keywords: ["CATALOG_STATUS_FULL_CRAWL","CATALOG_STATUS_IDLE","CATALOG_STATUS_INCREMENTAL_CRAWL","CATALOG_STATUS_PAUSED","CATALOG_STATUS_PROCESSING_NOTIFICATIONS","CATALOG_STATUS_RECOVERING","CATALOG_STATUS_SHUTTING_DOWN","CatalogStatus","CatalogStatus enumeration [search]","_search_CatalogStatus","search._search_CatalogStatus","searchapi/CATALOG_STATUS_FULL_CRAWL","searchapi/CATALOG_STATUS_IDLE","searchapi/CATALOG_STATUS_INCREMENTAL_CRAWL","searchapi/CATALOG_STATUS_PAUSED","searchapi/CATALOG_STATUS_PROCESSING_NOTIFICATIONS","searchapi/CATALOG_STATUS_RECOVERING","searchapi/CATALOG_STATUS_SHUTTING_DOWN","searchapi/CatalogStatus"]
old-location: search\_search_CatalogStatus.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\catalogstatus.htm
ms.date: 12/05/2018
ms.keywords: CATALOG_STATUS_FULL_CRAWL, CATALOG_STATUS_IDLE, CATALOG_STATUS_INCREMENTAL_CRAWL, CATALOG_STATUS_PAUSED, CATALOG_STATUS_PROCESSING_NOTIFICATIONS, CATALOG_STATUS_RECOVERING, CATALOG_STATUS_SHUTTING_DOWN, CatalogStatus, CatalogStatus enumeration [search], _search_CatalogStatus, search._search_CatalogStatus, searchapi/CATALOG_STATUS_FULL_CRAWL, searchapi/CATALOG_STATUS_IDLE, searchapi/CATALOG_STATUS_INCREMENTAL_CRAWL, searchapi/CATALOG_STATUS_PAUSED, searchapi/CATALOG_STATUS_PROCESSING_NOTIFICATIONS, searchapi/CATALOG_STATUS_RECOVERING, searchapi/CATALOG_STATUS_SHUTTING_DOWN, searchapi/CatalogStatus
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CatalogStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CatalogStatus
 - searchapi/_CatalogStatus
 - CatalogStatus
 - searchapi/CatalogStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - CatalogStatus
---

# CatalogStatus enumeration


## -description

Used by <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus">ISearchCatalogManager::GetCatalogStatus</a> to determine the current state of the catalog.

## -enum-fields

### -field CATALOG_STATUS_IDLE:0

Index is current; no indexing needed. Queries can be processed.

### -field CATALOG_STATUS_PAUSED:1

Indexer is paused. This can happen either because the user paused indexing or the indexer back-off criteria have been met. Queries can be processed.

### -field CATALOG_STATUS_RECOVERING:2

Index is recovering; queries and indexing are processed while in this state.

### -field CATALOG_STATUS_FULL_CRAWL:3

Indexer is currently executing a full crawl and will index everything it is configured to index. Queries can be processed while indexing.

### -field CATALOG_STATUS_INCREMENTAL_CRAWL:4

Indexer is preforming a crawl to see if anything has changed or requires indexing. Queries can be processed while indexing.

### -field CATALOG_STATUS_PROCESSING_NOTIFICATIONS:5

Indexer is processing the notification queue. This is done before resuming any crawl.

### -field CATALOG_STATUS_SHUTTING_DOWN:6

Indexer is shutting down and is not indexing.  Indexer can't be queried.
