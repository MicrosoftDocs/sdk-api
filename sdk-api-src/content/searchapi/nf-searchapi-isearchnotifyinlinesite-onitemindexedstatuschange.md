---
UID: NF:searchapi.ISearchNotifyInlineSite.OnItemIndexedStatusChange
title: ISearchNotifyInlineSite::OnItemIndexedStatusChange (searchapi.h)
description: Called by the search service to notify the client when the status of a particular document or item changes.
helpviewer_keywords: ["ISearchNotifyInlineSite interface [search]","OnItemIndexedStatusChange method","ISearchNotifyInlineSite.OnItemIndexedStatusChange","ISearchNotifyInlineSite::OnItemIndexedStatusChange","OnItemIndexedStatusChange","OnItemIndexedStatusChange method [search]","OnItemIndexedStatusChange method [search]","ISearchNotifyInlineSite interface","_search_ISearchNotifyInlineSite_OnItemIndexedStatusChange","search._search_ISearchNotifyInlineSite_OnItemIndexedStatusChange","searchapi/ISearchNotifyInlineSite::OnItemIndexedStatusChange"]
old-location: search\_search_ISearchNotifyInlineSite_OnItemIndexedStatusChange.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\onitemindexedstatuschange.htm
ms.date: 12/05/2018
ms.keywords: ISearchNotifyInlineSite interface [search],OnItemIndexedStatusChange method, ISearchNotifyInlineSite.OnItemIndexedStatusChange, ISearchNotifyInlineSite::OnItemIndexedStatusChange, OnItemIndexedStatusChange, OnItemIndexedStatusChange method [search], OnItemIndexedStatusChange method [search],ISearchNotifyInlineSite interface, _search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, search._search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, searchapi/ISearchNotifyInlineSite::OnItemIndexedStatusChange
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchntfyinlinesite.idl
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
 - ISearchNotifyInlineSite::OnItemIndexedStatusChange
 - searchapi/ISearchNotifyInlineSite::OnItemIndexedStatusChange
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
 - ISearchNotifyInlineSite.OnItemIndexedStatusChange
---

# ISearchNotifyInlineSite::OnItemIndexedStatusChange


## -description

Called by the search service to notify the client when the status of a particular document or item changes.

## -parameters

### -param sipStatus [in]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_indexing_phase">SEARCH_INDEXING_PHASE</a></b>

The <a href="/windows/desktop/api/searchapi/ne-searchapi-search_indexing_phase">SEARCH_INDEXING_PHASE</a> status of each document in the array being sent.

### -param dwNumEntries [in]

Type: <b>DWORD</b>

The number of entries in <i>rgItemStatusEntries</i>.

### -param rgItemStatusEntries [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_indexing_status">SEARCH_ITEM_INDEXING_STATUS</a>[]</b>

An array of <a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_indexing_status">SEARCH_ITEM_INDEXING_STATUS</a> structures containing status update information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchnotifyinlinesite">ISearchNotifyInlineSite</a>



<a href="/windows/desktop/search/-search-3x-wds-notifyingofchanges">Notifying the Index of Changes</a>