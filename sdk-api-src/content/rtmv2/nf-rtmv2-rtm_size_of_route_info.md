---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RTM_SIZE_OF_ROUTE_INFO macro


## -description


The 
<b>RTM_SIZE_OF_ROUTE_INFO</b> macro returns the size of the route information structure, 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>. The size of this structure is variable, and is based on the number of next hops associated with the route. Use this macro when allocating memory for route structures.


## -parameters




### -param NumHops

Specifies the number of next hops in the route structure.


## -remarks



If the client  only allocates one next hop per route, the client can allocate an 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure statically.

The macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define RTM_SIZE_OF_ROUTE_INFO(NumHops)                     \
    FIELD_OFFSET(RTM_ROUTE_INFO, NextHopsList.NumNextHops)

#define RTM_BASIC_ROUTE_INFO_SIZE                           \
    (RTM_BASIC_ROUTE_INFO_SIZE + (NumHops) *                \
     sizeof(RTM_NEXTHOP_HANDLE))
</pre>
</td>
</tr>
</table></span></div>


