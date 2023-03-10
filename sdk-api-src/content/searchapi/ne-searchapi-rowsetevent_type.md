---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0023_0002
title: ROWSETEVENT_TYPE (searchapi.h)
description: Describes the type of change to the rowset's data.
helpviewer_keywords: ["ROWSETEVENT_TYPE","ROWSETEVENT_TYPE enumeration [search]","ROWSETEVENT_TYPE_DATAEXPIRED","ROWSETEVENT_TYPE_FOREGROUNDLOST","ROWSETEVENT_TYPE_SCOPESTATISTICS","_search_ROWSETEVENT_TYPE","search._search_ROWSETEVENT_TYPE","searchapi/ROWSETEVENT_TYPE","searchapi/ROWSETEVENT_TYPE_DATAEXPIRED","searchapi/ROWSETEVENT_TYPE_FOREGROUNDLOST","searchapi/ROWSETEVENT_TYPE_SCOPESTATISTICS"]
old-location: search\_search_ROWSETEVENT_TYPE.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\rowsetevent_type.htm
ms.date: 12/05/2018
ms.keywords: ROWSETEVENT_TYPE, ROWSETEVENT_TYPE enumeration [search], ROWSETEVENT_TYPE_DATAEXPIRED, ROWSETEVENT_TYPE_FOREGROUNDLOST, ROWSETEVENT_TYPE_SCOPESTATISTICS, _search_ROWSETEVENT_TYPE, search._search_ROWSETEVENT_TYPE, searchapi/ROWSETEVENT_TYPE, searchapi/ROWSETEVENT_TYPE_DATAEXPIRED, searchapi/ROWSETEVENT_TYPE_FOREGROUNDLOST, searchapi/ROWSETEVENT_TYPE_SCOPESTATISTICS
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
req.typenames: ROWSETEVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_searchapi_0000_0023_0002
 - searchapi/__MIDL___MIDL_itf_searchapi_0000_0023_0002
 - ROWSETEVENT_TYPE
 - searchapi/ROWSETEVENT_TYPE
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
 - ROWSETEVENT_TYPE
---

# ROWSETEVENT_TYPE enumeration


## -description

Describes the type of change to the rowset's data.

## -enum-fields

### -field ROWSETEVENT_TYPE_DATAEXPIRED:0

Indicates that data backing the rowset has expired, and that a new rowset should be requested.

### -field ROWSETEVENT_TYPE_FOREGROUNDLOST:1

Indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.

### -field ROWSETEVENT_TYPE_SCOPESTATISTICS:2

Indicates that the scope statistics are to be obtained.

## -remarks

This enumeration is used in the <a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetevents-onrowsetevent">IRowsetEvents::OnRowsetEvent</a> method to describe the type of event that affects a rowset.

The <b>ROWSETEVENT_TYPE_SCOPESTATISTICS</b> event gives you the same information available from the <a href="/windows/desktop/api/searchapi/nf-searchapi-irowsetprioritization-getscopestatistics">IRowsetPrioritization::GetScopeStatistics</a> method call, but through a push mechanic, as follows: 

<ul>
<li>The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.  </li>
<li>The event arises only when statistics actually change, and the interval specified in the <a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a> has elapsed (the interval does not guarantee the frequency of the event).</li>
<li>This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</li>
<li>The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</li>
</ul>
Check out the <a href="/windows/win32/search/-search-sample-searchevents">SearchEvents code sample</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/desktop/search/-search-3x-wds-support">Notifications Process (Windows Search)</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
