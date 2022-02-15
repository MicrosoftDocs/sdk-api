---
UID: NF:searchapi.IRowsetEvents.OnRowsetEvent
title: IRowsetEvents::OnRowsetEvent (searchapi.h)
description: Called by the indexer to notify clients of an event related to the client rowset.
helpviewer_keywords: ["IRowsetEvents interface [search]","OnRowsetEvent method","IRowsetEvents.OnRowsetEvent","IRowsetEvents::OnRowsetEvent","OnRowsetEvent","OnRowsetEvent method [search]","OnRowsetEvent method [search]","IRowsetEvents interface","_search_IRowsetEvents_OnRowsetEvent","search._search_IRowsetEvents_OnRowsetEvent","searchapi/IRowsetEvents::OnRowsetEvent"]
old-location: search\_search_IRowsetEvents_OnRowsetEvent.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\irowsetevents\onrowsetevent.htm
ms.date: 12/05/2018
ms.keywords: IRowsetEvents interface [search],OnRowsetEvent method, IRowsetEvents.OnRowsetEvent, IRowsetEvents::OnRowsetEvent, OnRowsetEvent, OnRowsetEvent method [search], OnRowsetEvent method [search],IRowsetEvents interface, _search_IRowsetEvents_OnRowsetEvent, search._search_IRowsetEvents_OnRowsetEvent, searchapi/IRowsetEvents::OnRowsetEvent
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
 - IRowsetEvents::OnRowsetEvent
 - searchapi/IRowsetEvents::OnRowsetEvent
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
 - IRowsetEvents.OnRowsetEvent
---

# IRowsetEvents::OnRowsetEvent


## -description

Called by the indexer to notify clients of an event related to the client rowset.

## -parameters

### -param eventType [in]

Type: <b><a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a></b>

The event triggering the notification as the <a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a> enumeration.

### -param eventData [in]

Type: <b>REFPROPVARIANT</b>

The expected value of the event data for the event type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

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