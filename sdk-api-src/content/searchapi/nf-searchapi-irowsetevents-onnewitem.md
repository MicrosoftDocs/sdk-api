---
UID: NF:searchapi.IRowsetEvents.OnNewItem
title: IRowsetEvents::OnNewItem (searchapi.h)
description: Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.
helpviewer_keywords: ["IRowsetEvents interface [search]","OnNewItem method","IRowsetEvents.OnNewItem","IRowsetEvents::OnNewItem","OnNewItem","OnNewItem method [search]","OnNewItem method [search]","IRowsetEvents interface","_search_IRowsetEvents_OnNewItem","search._search_IRowsetEvents_OnNewItem","searchapi/IRowsetEvents::OnNewItem"]
old-location: search\_search_IRowsetEvents_OnNewItem.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onnewitem.htm
ms.date: 12/05/2018
ms.keywords: IRowsetEvents interface [search],OnNewItem method, IRowsetEvents.OnNewItem, IRowsetEvents::OnNewItem, OnNewItem, OnNewItem method [search], OnNewItem method [search],IRowsetEvents interface, _search_IRowsetEvents_OnNewItem, search._search_IRowsetEvents_OnNewItem, searchapi/IRowsetEvents::OnNewItem
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRowsetEvents::OnNewItem
 - searchapi/IRowsetEvents::OnNewItem
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
 - IRowsetEvents.OnNewItem
---

# IRowsetEvents::OnNewItem


## -description

Called by the indexer to notify clients of a new item that may match some (or all) of the criteria for the client rowset.

## -parameters

### -param itemID [in]

Type: <b>REFPROPVARIANT</b>

The new item that may match the original search criteria of the rowset.

### -param newItemState [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a></b>

Specifies whether the new item matches all or some of the criteria for your rowset, as a <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a> indicates the degree to which the new item may match the original search criteria of a rowset:
        

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the new item definitely matches all criteria for your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the new item at least partially matches some criteria for your rowset. It may match fully.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> is not applicable for new items.</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>