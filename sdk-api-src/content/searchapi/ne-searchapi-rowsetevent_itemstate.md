---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0023_0001
title: ROWSETEVENT_ITEMSTATE (searchapi.h)
description: Describes whether an item that matches the search criteria of a rowset is currently in that rowset.
helpviewer_keywords: ["ROWSETEVENT_ITEMSTATE","ROWSETEVENT_ITEMSTATE enumeration [search]","ROWSETEVENT_ITEMSTATE_INROWSET","ROWSETEVENT_ITEMSTATE_NOTINROWSET","ROWSETEVENT_ITEMSTATE_UNKNOWN","_search_ROWSETEVENT_ITEMSTATE","search._search_ROWSETEVENT_ITEMSTATE","searchapi/ROWSETEVENT_ITEMSTATE","searchapi/ROWSETEVENT_ITEMSTATE_INROWSET","searchapi/ROWSETEVENT_ITEMSTATE_NOTINROWSET","searchapi/ROWSETEVENT_ITEMSTATE_UNKNOWN"]
old-location: search\_search_ROWSETEVENT_ITEMSTATE.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\rowsetevent_itemstate.htm
ms.date: 12/05/2018
ms.keywords: ROWSETEVENT_ITEMSTATE, ROWSETEVENT_ITEMSTATE enumeration [search], ROWSETEVENT_ITEMSTATE_INROWSET, ROWSETEVENT_ITEMSTATE_NOTINROWSET, ROWSETEVENT_ITEMSTATE_UNKNOWN, _search_ROWSETEVENT_ITEMSTATE, search._search_ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE_INROWSET, searchapi/ROWSETEVENT_ITEMSTATE_NOTINROWSET, searchapi/ROWSETEVENT_ITEMSTATE_UNKNOWN
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
req.typenames: ROWSETEVENT_ITEMSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_searchapi_0000_0023_0001
 - searchapi/__MIDL___MIDL_itf_searchapi_0000_0023_0001
 - ROWSETEVENT_ITEMSTATE
 - searchapi/ROWSETEVENT_ITEMSTATE
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
 - ROWSETEVENT_ITEMSTATE
---

# ROWSETEVENT_ITEMSTATE enumeration


## -description

Describes whether an item that matches the search criteria of a rowset is currently in that rowset.

## -enum-fields

### -field ROWSETEVENT_ITEMSTATE_NOTINROWSET:0

The item is definitely not in the rowset.

### -field ROWSETEVENT_ITEMSTATE_INROWSET:1

The item is definitely contained within the rowset.

### -field ROWSETEVENT_ITEMSTATE_UNKNOWN:2

The item may be in the rowset.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetevents">IRowsetEvents</a> to describe the state of rows in a rowset held by a client.

Check out the <a href="/windows/win32/search/-search-sample-searchevents">SearchEvents code sample</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
