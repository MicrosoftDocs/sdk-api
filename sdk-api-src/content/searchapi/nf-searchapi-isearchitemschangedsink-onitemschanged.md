---
UID: NF:searchapi.ISearchItemsChangedSink.OnItemsChanged
title: ISearchItemsChangedSink::OnItemsChanged (searchapi.h)
description: Call this method to notify an indexer to re-index some changed items.
helpviewer_keywords: ["ISearchItemsChangedSink interface [search]","OnItemsChanged method","ISearchItemsChangedSink.OnItemsChanged","ISearchItemsChangedSink::OnItemsChanged","OnItemsChanged","OnItemsChanged method [search]","OnItemsChanged method [search]","ISearchItemsChangedSink interface","_search_ISearchItemsChangedSink_OnItemsChanged","search._search_ISearchItemsChangedSink_OnItemsChanged","searchapi/ISearchItemsChangedSink::OnItemsChanged"]
old-location: search\_search_ISearchItemsChangedSink_OnItemsChanged.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchitemschangedsink\onitemschanged.htm
ms.date: 12/05/2018
ms.keywords: ISearchItemsChangedSink interface [search],OnItemsChanged method, ISearchItemsChangedSink.OnItemsChanged, ISearchItemsChangedSink::OnItemsChanged, OnItemsChanged, OnItemsChanged method [search], OnItemsChanged method [search],ISearchItemsChangedSink interface, _search_ISearchItemsChangedSink_OnItemsChanged, search._search_ISearchItemsChangedSink_OnItemsChanged, searchapi/ISearchItemsChangedSink::OnItemsChanged
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ISearchItemsChangedSink::OnItemsChanged
 - searchapi/ISearchItemsChangedSink::OnItemsChanged
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
 - ISearchItemsChangedSink.OnItemsChanged
---

# ISearchItemsChangedSink::OnItemsChanged


## -description

   
            Call this method to notify an indexer to re-index some changed items.

## -parameters

### -param dwNumberOfChanges [in]

Type: <b>DWORD</b>

The number of items that have changed.

### -param rgDataChangeEntries [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_change">SEARCH_ITEM_CHANGE</a>[]</b>

An array of <a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_change">SEARCH_ITEM_CHANGE</a> structures, describing the type of changes to and the paths or URLs of each item.

### -param rgdwDocIds [out]

Type: <b>DWORD[]</b>

Receives a pointer to an array of document identifiers for the items that changed.

### -param rghrCompletionCodes [out]

Type: <b>HRESULT[]</b>

Receives a pointer to an array of completion codes for <i>rgdwDocIds</i> indicating whether each item was accepted for indexing.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When there are multiple change notifications, the <b>priority</b> member of the <a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_change">SEARCH_ITEM_CHANGE</a> structure indicates the priority of processing.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink">ISearchItemsChangedSink</a>



<a href="/windows/desktop/search/-search-3x-wds-notifyingofchanges">Notifying the Index of Changes</a>