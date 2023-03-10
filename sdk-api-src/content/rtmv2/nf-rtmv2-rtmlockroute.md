---
UID: NF:rtmv2.RtmLockRoute
title: RtmLockRoute function (rtmv2.h)
description: The RtmLockRoute function locks or unlocks a route in the routing table. This protects the route while a client makes the necessary changes to the opaque route pointers owned by the client.
helpviewer_keywords: ["RtmLockRoute","RtmLockRoute function [RAS]","_rtmv2ref_rtmlockroute","rras.rtmlockroute","rtmv2/RtmLockRoute"]
old-location: rras\rtmlockroute.htm
tech.root: RRAS
ms.assetid: 8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f
ms.date: 12/05/2018
ms.keywords: RtmLockRoute, RtmLockRoute function [RAS], _rtmv2ref_rtmlockroute, rras.rtmlockroute, rtmv2/RtmLockRoute
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmLockRoute
 - rtmv2/RtmLockRoute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmLockRoute
---

# RtmLockRoute function


## -description

The 
<b>RtmLockRoute</b> function locks or unlocks a route in the routing table. This protects the route while a client makes the necessary changes to the opaque route pointers owned by the client.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

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
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>.

Currently, this function locks the entire destination, not just the route.

Clients can only change the <b>Neighbour</b>, <b>PrefInfo</b>, <b>BelongsToViews</b>, <b>EntitySpecificInfo</b>, and <b>NextHopsList</b> members of the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure.

If any of these values are changed, the client must call 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a> to notify the routing table manager of the changes.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutetodest">RtmDeleteRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetroutepointer">RtmGetRoutePointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmholddestination">RtmHoldDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>