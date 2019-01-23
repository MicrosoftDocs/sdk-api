---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0023_0001
title: ROWSETEVENT_ITEMSTATE
author: windows-sdk-content
description: Describes whether an item that matches the search criteria of a rowset is currently in that rowset.
old-location: search\_search_ROWSETEVENT_ITEMSTATE.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\rowsetevent_itemstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ROWSETEVENT_ITEMSTATE, ROWSETEVENT_ITEMSTATE enumeration [search], ROWSETEVENT_ITEMSTATE_INROWSET, ROWSETEVENT_ITEMSTATE_NOTINROWSET, ROWSETEVENT_ITEMSTATE_UNKNOWN, _search_ROWSETEVENT_ITEMSTATE, search._search_ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE_INROWSET, searchapi/ROWSETEVENT_ITEMSTATE_NOTINROWSET, searchapi/ROWSETEVENT_ITEMSTATE_UNKNOWN
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - ROWSETEVENT_ITEMSTATE
product: Windows
targetos: Windows
req.typenames: ROWSETEVENT_ITEMSTATE
req.redist: 
---

# ROWSETEVENT_ITEMSTATE enumeration


## -description


Describes whether an item that matches the search criteria of a rowset is currently in that rowset.


## -enum-fields




### -field ROWSETEVENT_ITEMSTATE_NOTINROWSET

The item is definitely not in the rowset.
            


### -field ROWSETEVENT_ITEMSTATE_INROWSET

The item is definitely contained within the rowset.
            


### -field ROWSETEVENT_ITEMSTATE_UNKNOWN

The item may be in the rowset.
            


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/en-us/library/Dd318749(v=VS.85).aspx">IRowsetEvents</a> to describe the state of rows in a rowset held by a client.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Dd318747(v=VS.85).aspx">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb288457(v=VS.85).aspx">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc142933(v=VS.85).aspx">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd797839(v=VS.85).aspx">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368862(v=VS.85).aspx">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Cc465173(v=VS.85).aspx">Rowset Properties</a>
 

 

