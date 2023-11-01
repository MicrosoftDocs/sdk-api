---
UID: NF:searchapi.IRowsetEvents.OnChangedItem
title: IRowsetEvents::OnChangedItem (searchapi.h)
description: Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.
helpviewer_keywords: ["IRowsetEvents interface [search]","OnChangedItem method","IRowsetEvents.OnChangedItem","IRowsetEvents::OnChangedItem","OnChangedItem","OnChangedItem method [search]","OnChangedItem method [search]","IRowsetEvents interface","_search_IRowsetEvents_OnChangedItem","search._search_IRowsetEvents_OnChangedItem","searchapi/IRowsetEvents::OnChangedItem"]
old-location: search\_search_IRowsetEvents_OnChangedItem.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onchangeditem.htm
ms.date: 12/05/2018
ms.keywords: IRowsetEvents interface [search],OnChangedItem method, IRowsetEvents.OnChangedItem, IRowsetEvents::OnChangedItem, OnChangedItem, OnChangedItem method [search], OnChangedItem method [search],IRowsetEvents interface, _search_IRowsetEvents_OnChangedItem, search._search_IRowsetEvents_OnChangedItem, searchapi/IRowsetEvents::OnChangedItem
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
 - IRowsetEvents::OnChangedItem
 - searchapi/IRowsetEvents::OnChangedItem
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
 - IRowsetEvents.OnChangedItem
---

# IRowsetEvents::OnChangedItem


## -description

Called by the indexer to notify clients that an item has been modified. This item may have matched some (or all) of the criteria for the client rowset.

## -parameters

### -param itemID [in]

Type: <b>REFPROPVARIANT</b>

Specifies the item in the rowset that has changed.

### -param rowsetItemState [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a></b>

Specifies whether the changed item was originally in the rowset.

### -param changedItemState [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a></b>

Specifies whether the changed item is currently in the rowset, as a result of the change.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a> for <i>rowsetItemState</i> indicates whether the item was contained in the original rowset: 

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the item is definitely contained within your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the item may be contained within your rowset. The containment status is not known because your rowset is not fully evaluated.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> indicates that the item was not originally in your rowset</li>
</ul>
The <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a> for <i>changedItemState</i> indicates whether the newly modified item now matches the degree to which the new item may match the original search criteria of a rowset: 

<ul>
<li><i>ROWSETEVENT_ITEMSTATE_INROWSET</i> indicates that the item definitely belongs in your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_UNKNOWN</i> indicates that the item may now belong in your rowset.</li>
<li><i>ROWSETEVENT_ITEMSTATE_NOTINROWSET</i> indicates that the item does not belong in your rowset.</li>
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