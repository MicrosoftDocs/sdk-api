---
UID: NF:searchapi.ISearchCatalogManager.NumberOfItemsToIndex
title: ISearchCatalogManager::NumberOfItemsToIndex (searchapi.h)
description: Gets the number of items to be indexed within the catalog.helpviewer_keywords: ["ISearchCatalogManager interface [search]","NumberOfItemsToIndex method","ISearchCatalogManager.NumberOfItemsToIndex","ISearchCatalogManager::NumberOfItemsToIndex","NumberOfItemsToIndex","NumberOfItemsToIndex method [search]","NumberOfItemsToIndex method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_NumberOfItemsToIndex","search._search_ISearchCatalogManager_NumberOfItemsToIndex","searchapi/ISearchCatalogManager::NumberOfItemsToIndex"]
old-location: search\_search_ISearchCatalogManager_NumberOfItemsToIndex.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\numberofitemstoindex.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],NumberOfItemsToIndex method, ISearchCatalogManager.NumberOfItemsToIndex, ISearchCatalogManager::NumberOfItemsToIndex, NumberOfItemsToIndex, NumberOfItemsToIndex method [search], NumberOfItemsToIndex method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_NumberOfItemsToIndex, search._search_ISearchCatalogManager_NumberOfItemsToIndex, searchapi/ISearchCatalogManager::NumberOfItemsToIndex
ms.topic: method
f1_keywords:
- searchapi/ISearchCatalogManager.NumberOfItemsToIndex
dev_langs:
- c++
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchCatalogManager.NumberOfItemsToIndex
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCatalogManager::NumberOfItemsToIndex


## -description


Gets the number of items to be indexed within the catalog.
        


## -parameters




### -param plIncrementalCount [out]

Type: <b>LONG*</b>

Receives a pointer to the number of items to be indexed in the next incremental index.
                


### -param plNotificationQueue [out]

Type: <b>LONG*</b>

Receives a pointer to the number of items in the notification queue.
                


### -param plHighPriorityQueue [out]

Type: <b>LONG*</b>

Receives a pointer to the number of items in the high-priority queue. Items in the <i>plHighPriorityQueue</i> are indexed first.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



