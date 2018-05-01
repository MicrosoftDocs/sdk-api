---
UID: NF:rtmv2.RtmDeleteNextHop
title: RtmDeleteNextHop function
author: windows-driver-content
description: The RtmDeleteNextHop function deletes a next hop from the next-hop list.
old-location: rras\rtmdeletenexthop.htm
old-project: RRAS
ms.assetid: 708a890e-4dc6-49c7-b857-cdb8504e7f7f
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RtmDeleteNextHop, RtmDeleteNextHop function [RAS], _rtmv2ref_rtmdeletenexthop, rras.rtmdeletenexthop, rtmv2/RtmDeleteNextHop
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmDeleteNextHop
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmDeleteNextHop function


## -description


The 
<b>RtmDeleteNextHop</b> function deletes a next hop from the next-hop list.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param OPTIONAL

TBD


### -param NextHopInfo [in]

Pointer to a structure that contains information identifying the next hop to delete. This parameter is optional and can be set to <b>NULL</b>; if it is <b>NULL</b>, the handle in <i>NextHopHandle</i> is used to identify the next hop to delete.


#### - NextHopHandle [in]

Handle to the next hop to delete. This parameter is optional and can be set to <b>NULL</b>; if it is <b>NULL</b>, the values in <i>NextHopInfo</i> are used to identify the next hop to delete.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling client does not own this next hop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified next hop was not found.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



If a client specifies a <i>NextHopHandle</i>, the client should not subsequently release the handle using 
<a href="https://msdn.microsoft.com/a21de428-7e9d-4596-a7ab-06a29b9852f7">RtmReleaseNextHops</a>.




## -see-also




<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/7c11397b-f5c9-4a3e-88d8-2f1736f5da13">RtmAddNextHop</a>



<a href="https://msdn.microsoft.com/82bf88ad-eb6d-4ea5-98a0-72280e341f83">RtmFindNextHop</a>



<a href="https://msdn.microsoft.com/61fa3fa2-1cad-4930-975e-8f5b86ad3b05">RtmGetNextHopPointer</a>
 

 

