---
UID: NF:searchapi.ISearchCatalogManager.GetPersistentItemsChangedSink
title: ISearchCatalogManager::GetPersistentItemsChangedSink (searchapi.h)
description: Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.
helpviewer_keywords: ["GetPersistentItemsChangedSink","GetPersistentItemsChangedSink method [search]","GetPersistentItemsChangedSink method [search]","ISearchCatalogManager interface","ISearchCatalogManager interface [search]","GetPersistentItemsChangedSink method","ISearchCatalogManager.GetPersistentItemsChangedSink","ISearchCatalogManager::GetPersistentItemsChangedSink","_search_ISearchCatalogManager_GetPersistentItemsChangedSink","search._search_ISearchCatalogManager_GetPersistentItemsChangedSink","searchapi/ISearchCatalogManager::GetPersistentItemsChangedSink"]
old-location: search\_search_ISearchCatalogManager_GetPersistentItemsChangedSink.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getpersistentitemschangedsink.htm
ms.date: 12/05/2018
ms.keywords: GetPersistentItemsChangedSink, GetPersistentItemsChangedSink method [search], GetPersistentItemsChangedSink method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetPersistentItemsChangedSink method, ISearchCatalogManager.GetPersistentItemsChangedSink, ISearchCatalogManager::GetPersistentItemsChangedSink, _search_ISearchCatalogManager_GetPersistentItemsChangedSink, search._search_ISearchCatalogManager_GetPersistentItemsChangedSink, searchapi/ISearchCatalogManager::GetPersistentItemsChangedSink
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchCatalogManager::GetPersistentItemsChangedSink
 - searchapi/ISearchCatalogManager::GetPersistentItemsChangedSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager.GetPersistentItemsChangedSink
---

# ISearchCatalogManager::GetPersistentItemsChangedSink


## -description

Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.

## -parameters

### -param ppISearchPersistentItemsChangedSink [out, retval]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink">ISearchPersistentItemsChangedSink</a>**</b>

Receives the address of a pointer to a new <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink">ISearchPersistentItemsChangedSink</a> interface for this catalog.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.