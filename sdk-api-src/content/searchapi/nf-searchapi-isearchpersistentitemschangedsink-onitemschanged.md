---
UID: NF:searchapi.ISearchPersistentItemsChangedSink.OnItemsChanged
title: ISearchPersistentItemsChangedSink::OnItemsChanged (searchapi.h)
description: Notifies the indexer to index changed items.
helpviewer_keywords: ["ISearchPersistentItemsChangedSink interface [search]","OnItemsChanged method","ISearchPersistentItemsChangedSink.OnItemsChanged","ISearchPersistentItemsChangedSink::OnItemsChanged","OnItemsChanged","OnItemsChanged method [search]","OnItemsChanged method [search]","ISearchPersistentItemsChangedSink interface","_search_ISearchPersistentItemsChangedSink_OnItemsChanged","search._search_ISearchPersistentItemsChangedSink_OnItemsChanged","searchapi/ISearchPersistentItemsChangedSink::OnItemsChanged"]
old-location: search\_search_ISearchPersistentItemsChangedSink_OnItemsChanged.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchpersistentitemschangedsink\onitemschanged.htm
ms.date: 12/05/2018
ms.keywords: ISearchPersistentItemsChangedSink interface [search],OnItemsChanged method, ISearchPersistentItemsChangedSink.OnItemsChanged, ISearchPersistentItemsChangedSink::OnItemsChanged, OnItemsChanged, OnItemsChanged method [search], OnItemsChanged method [search],ISearchPersistentItemsChangedSink interface, _search_ISearchPersistentItemsChangedSink_OnItemsChanged, search._search_ISearchPersistentItemsChangedSink_OnItemsChanged, searchapi/ISearchPersistentItemsChangedSink::OnItemsChanged
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchnotifications.idl
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
 - ISearchPersistentItemsChangedSink::OnItemsChanged
 - searchapi/ISearchPersistentItemsChangedSink::OnItemsChanged
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
 - ISearchPersistentItemsChangedSink.OnItemsChanged
---

# ISearchPersistentItemsChangedSink::OnItemsChanged


## -description

Notifies the indexer to index changed items.

## -parameters

### -param dwNumberOfChanges [in]

Type: <b>DWORD</b>

The number of changes being reported.

### -param DataChangeEntries [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_persistent_change">SEARCH_ITEM_PERSISTENT_CHANGE</a>[]</b>

An array of structures of type <a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_persistent_change">SEARCH_ITEM_PERSISTENT_CHANGE</a> identifying the details for each change.

### -param hrCompletionCodes [out]

Type: <b>HRESULT[]</b>

Indicates whether each URL was accepted for indexing.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.