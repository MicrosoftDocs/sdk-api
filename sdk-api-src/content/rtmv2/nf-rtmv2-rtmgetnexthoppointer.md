---
UID: NF:rtmv2.RtmGetNextHopPointer
title: RtmGetNextHopPointer function
author: windows-sdk-content
description: The RtmGetNextHopPointer function obtains a direct pointer to the specified next hop. The pointer allows the next-hop owner direct read access to the routing table manager's RTM_NEXTHOP_INFO structure.
old-location: rras\rtmgetnexthoppointer.htm
tech.root: rras
ms.assetid: 61fa3fa2-1cad-4930-975e-8f5b86ad3b05
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: RtmGetNextHopPointer, RtmGetNextHopPointer function [RAS], _rtmv2ref_rtmgetnexthoppointer, rras.rtmgetnexthoppointer, rtmv2/RtmGetNextHopPointer
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmGetNextHopPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmGetNextHopPointer function


## -description


The 
<b>RtmGetNextHopPointer</b> function obtains a direct pointer to the specified next hop. The pointer allows the next-hop owner direct read access to the routing table manager's 
<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a> structure.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NextHopHandle [in]

Handle to the next hop.


### -param NextHopPointer [out]

If the client is the owner of the next hop, <i>NextHopPointer</i> receives a pointer to the next hop.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



Clients should only use this pointer for read-only access.

When the next hop handle is no longer required, release it by calling 
<a href="https://msdn.microsoft.com/1c5a9b72-8605-4c54-bc44-b7a1a4e1b367">RtmReleaseNextHopInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/17705e5b-0905-45a5-b76e-e381e863a1ea">RTM_NEXTHOP_INFO</a>



<a href="https://msdn.microsoft.com/7c11397b-f5c9-4a3e-88d8-2f1736f5da13">RtmAddNextHop</a>



<a href="https://msdn.microsoft.com/708a890e-4dc6-49c7-b857-cdb8504e7f7f">RtmDeleteNextHop</a>



<a href="https://msdn.microsoft.com/82bf88ad-eb6d-4ea5-98a0-72280e341f83">RtmFindNextHop</a>



<a href="https://msdn.microsoft.com/f5b6d430-a50e-49fc-8274-81bac1300477">RtmLockNextHop</a>
 

 

