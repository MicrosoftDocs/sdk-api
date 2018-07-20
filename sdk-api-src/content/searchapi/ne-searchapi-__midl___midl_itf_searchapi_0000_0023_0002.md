---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0023_0002
title: "__MIDL___MIDL_itf_searchapi_0000_0023_0002"
author: windows-sdk-content
description: Describes the type of change to the rowset's data.
old-location: search\_search_ROWSETEVENT_TYPE.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\rowsetevent_type.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ROWSETEVENT_TYPE, ROWSETEVENT_TYPE enumeration [search], ROWSETEVENT_TYPE_DATAEXPIRED, ROWSETEVENT_TYPE_FOREGROUNDLOST, ROWSETEVENT_TYPE_SCOPESTATISTICS, __MIDL___MIDL_itf_searchapi_0000_0023_0002, _search_ROWSETEVENT_TYPE, search._search_ROWSETEVENT_TYPE, searchapi/ROWSETEVENT_TYPE, searchapi/ROWSETEVENT_TYPE_DATAEXPIRED, searchapi/ROWSETEVENT_TYPE_FOREGROUNDLOST, searchapi/ROWSETEVENT_TYPE_SCOPESTATISTICS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - ROWSETEVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
---

# __MIDL___MIDL_itf_searchapi_0000_0023_0002 enumeration


## -description


Describes the type of change to the rowset's data.


## -enum-fields




### -field ROWSETEVENT_TYPE_DATAEXPIRED


                Indicates that data backing the rowset has expired, and that a new rowset should be requested.
            


### -field ROWSETEVENT_TYPE_FOREGROUNDLOST


                Indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.
            


### -field ROWSETEVENT_TYPE_SCOPESTATISTICS


                Indicates that the scope statistics are to be optained.
            


## -remarks



This enumeration is used in the <a href="https://msdn.microsoft.com/91f458c5-476f-41fb-bb04-4936440f7b1e">IRowsetEvents::OnRowsetEvent</a> method to describe the type of event that affects a rowset.

The <b>ROWSETEVENT_TYPE_SCOPESTATISTICS</b> event gives you the same information available from the <a href="https://msdn.microsoft.com/82d64fe6-6264-4262-a778-bf30a62dcecb">IRowsetPrioritization::GetScopeStatistics</a> method call, but through a push mechanic, as follows: 

<ul>
<li>The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.  </li>
<li>The event arises only when statistics actually change, and the interval specified in the <a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a> has elapsed (the interval does not guarantee the frequency of the event).</li>
<li>This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</li>
<li>The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</li>
</ul>
The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/378e346b-2067-484f-85e9-76673a35550b">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/d172ae7f-a495-4ea4-9d7d-ca8065f8d3cb">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71aa0ad6-ef34-47ee-945f-04bda20bf8a4">Rowset Properties</a>
 

 

