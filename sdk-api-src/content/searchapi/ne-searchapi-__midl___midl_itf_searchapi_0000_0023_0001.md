---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0023_0001
title: "__MIDL___MIDL_itf_searchapi_0000_0023_0001"
author: windows-driver-content
description: Describes whether an item that matches the search criteria of a rowset is currently in that rowset.
old-location: search\_search_ROWSETEVENT_ITEMSTATE.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\rowsetevent_itemstate.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ROWSETEVENT_ITEMSTATE, ROWSETEVENT_ITEMSTATE enumeration [search], ROWSETEVENT_ITEMSTATE_INROWSET, ROWSETEVENT_ITEMSTATE_NOTINROWSET, ROWSETEVENT_ITEMSTATE_UNKNOWN, __MIDL___MIDL_itf_searchapi_0000_0023_0001, _search_ROWSETEVENT_ITEMSTATE, search._search_ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE, searchapi/ROWSETEVENT_ITEMSTATE_INROWSET, searchapi/ROWSETEVENT_ITEMSTATE_NOTINROWSET, searchapi/ROWSETEVENT_ITEMSTATE_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROWSETEVENT_ITEMSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	ROWSETEVENT_ITEMSTATE
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_searchapi_0000_0023_0001 enumeration


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



This enumeration is used by <a href="https://msdn.microsoft.com/df16492c-e8f9-4d01-a8ad-cd76ea6bbc73">IRowsetEvents</a> to describe the state of rows in a rowset held by a client.

The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/378e346b-2067-484f-85e9-76673a35550b">Notifications Process (Windows Search)</a>



<a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/d172ae7f-a495-4ea4-9d7d-ca8065f8d3cb">PRIORITY_LEVEL</a>



<a href="https://msdn.microsoft.com/c9fb74f6-8aed-4450-9bc4-d9f5c3e835a4">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71aa0ad6-ef34-47ee-945f-04bda20bf8a4">Rowset Properties</a>
 

 

