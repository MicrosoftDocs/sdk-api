---
UID: NF:rtmv2.RtmLockRoute
title: RtmLockRoute function
author: windows-sdk-content
description: The RtmLockRoute function locks or unlocks a route in the routing table. This protects the route while a client makes the necessary changes to the opaque route pointers owned by the client.
old-location: rras\rtmlockroute.htm
tech.root: rras
ms.assetid: 8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: RtmLockRoute, RtmLockRoute function [RAS], _rtmv2ref_rtmlockroute, rras.rtmlockroute, rtmv2/RtmLockRoute
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
 - RtmLockRoute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmLockRoute function


## -description


The 
<b>RtmLockRoute</b> function locks or unlocks a route in the routing table. This protects the route while a client makes the necessary changes to the opaque route pointers owned by the client.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteHandle [in]

Handle to the route to lock.


### -param Exclusive [in]

Specifies whether to lock or unlock the route in an exclusive (<b>TRUE</b>) or shared (<b>FALSE</b>) mode.


### -param LockRoute [in]

Specifies whether to lock or unlock the route. Specify <b>TRUE</b> to lock the route; specify <b>FALSE</b> to unlock it.


### -param RoutePointer [out]

If a pointer must be returned: On input, <i>RoutePointer</i> is a pointer to <b>NULL</b>. On output, if the client owns the route, <i>RoutePointer</i> receives a pointer to the next-hop; otherwise, <i>RoutePointer</i> remains unchanged. 




If a handle does not need to be returned: On input, <i>RoutePointer</i> is <b>NULL</b>.


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
The calling client does not own this route.

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



Do not call any other RTMv2 functions until the route is unlocked by a call to 
<b>RtmLockRoute</b> and the <i>LockRoute</i> parameter is set to <b>FALSE</b>, or a call to 
<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a>.

Currently, this function locks the entire destination, not just the route.

Clients can only change the <b>Neighbour</b>, <b>PrefInfo</b>, <b>BelongsToViews</b>, <b>EntitySpecificInfo</b>, and <b>NextHopsList</b> members of the 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure.

If any of these values are changed, the client must call 
<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a> to notify the routing table manager of the changes.




## -see-also




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/d82e68b4-aff4-4872-b719-d9354f35024c">RtmDeleteRouteToDest</a>



<a href="https://msdn.microsoft.com/889e318c-b515-48bc-9117-83e8c1bb6f1a">RtmGetRoutePointer</a>



<a href="https://msdn.microsoft.com/433d6d97-9541-496a-8d10-2a2fc31d043d">RtmHoldDestination</a>



<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a>
 

 

