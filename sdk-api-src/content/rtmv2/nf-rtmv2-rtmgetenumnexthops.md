---
UID: NF:rtmv2.RtmGetEnumNextHops
title: RtmGetEnumNextHops function
author: windows-sdk-content
description: The RtmGetEnumNextHops function retrieves the next set of next hops in the specified enumeration.
old-location: rras\rtmgetenumnexthops.htm
old-project: RRAS
ms.assetid: 3e1a6064-6ba0-4ed8-b6df-1c347b098807
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RtmGetEnumNextHops, RtmGetEnumNextHops function [RAS], _rtmv2ref_rtmgetenumnexthops, rras.rtmgetenumnexthops, rtmv2/RtmGetEnumNextHops
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmGetEnumNextHops
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: ADAM
---

# RtmGetEnumNextHops function


## -description


The 
<b>RtmGetEnumNextHops</b> function retrieves the next set of next hops in the specified enumeration.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EnumHandle [in]

Handle to the next-hop enumeration.


### -param NumNextHops [in, out]

On input, <i>NumNextHops</i> is a pointer to a <b>UINT</b> value specifying the maximum number of next hops that can be received by <i>NextHopHandles</i>. 




On output, <i>NumNextHops</i> receives the actual number of next hops received by <i>NextHopHandles</i>.


### -param NextHopHandles [out]

On input, <i>NextHopHandles</i> pointers to an 
<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a> structure. 




On output, <i>NextHopHandles</i> receives an array of handles to next hops.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>NumRoutes</i> is larger than the maximum number of routes a client is allowed to retrieve with one call. Check 
<a href="https://msdn.microsoft.com/26644a09-8d49-4c9f-a7cd-5edbf93e83d0">RTM_REGN_PROFILE</a> for the maximum number of next hops that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more next hops to enumerate.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



When the next hops are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/a21de428-7e9d-4596-a7ab-06a29b9852f7">RtmReleaseNextHops</a>.




## -see-also




<a href="https://msdn.microsoft.com/d26ce475-ea05-4e84-92da-06df9c386858">RtmCreateNextHopEnum</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/a21de428-7e9d-4596-a7ab-06a29b9852f7">RtmReleaseNextHops</a>
 

 

