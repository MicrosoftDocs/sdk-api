---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CatalogStatus enumeration


## -description


Used by <a href="https://msdn.microsoft.com/22cd866e-8af7-428a-8036-43f5ac9ad099">ISearchCatalogManager::GetCatalogStatus</a> to determine the current state of the catalog.


## -enum-fields




### -field CATALOG_STATUS_IDLE

Index is current; no indexing needed. Queries can be processed.


### -field CATALOG_STATUS_PAUSED

Indexer is paused. This can happen either because the user paused indexing or the indexer back-off criteria have been met. Queries can be processed.


### -field CATALOG_STATUS_RECOVERING

Index is recovering; queries and indexing are processed while in this state.


### -field CATALOG_STATUS_FULL_CRAWL

Indexer is currently executing a full crawl and will index everything it is configured to index. Queries can be processed while indexing.


### -field CATALOG_STATUS_INCREMENTAL_CRAWL

Indexer is preforming a crawl to see if anything has changed or requires indexing. Queries can be processed while indexing.


### -field CATALOG_STATUS_PROCESSING_NOTIFICATIONS

Indexer is processing the notification queue. This is done before resuming any crawl.


### -field CATALOG_STATUS_SHUTTING_DOWN

Indexer is shutting down and is not indexing.  Indexer can't be queried.

