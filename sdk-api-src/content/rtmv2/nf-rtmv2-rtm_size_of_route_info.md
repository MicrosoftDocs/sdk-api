---
UID: NF:rtmv2.RTM_SIZE_OF_ROUTE_INFO
title: RTM_SIZE_OF_ROUTE_INFO macro
author: windows-sdk-content
description: The RTM_SIZE_OF_ROUTE_INFO macro returns the size of the route information structure, RTM_ROUTE_INFO.
old-location: rras\rtm_size_of_route_info.htm
tech.root: rras
ms.assetid: ef3308a1-9a5e-4162-91d1-6ae2abff5c3b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RTM_SIZE_OF_ROUTE_INFO, RTM_SIZE_OF_ROUTE_INFO macro [RAS], _rtmv2ref_rtm_size_of_route_info, rras.rtm_size_of_route_info, rtmv2/RTM_SIZE_OF_ROUTE_INFO
ms.topic: macro
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Rtmv2.h
api_name:
 - RTM_SIZE_OF_ROUTE_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


