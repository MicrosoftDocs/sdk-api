---
UID: NF:rtmv2.RtmUpdateAndUnlockRoute
title: RtmUpdateAndUnlockRoute function (rtmv2.h)
description: The RtmUpdateAndUnlockRoute function updates the position of the route in the set of routes for a destination, and adjusts the best route information for the destination.
helpviewer_keywords: ["RtmUpdateAndUnlockRoute","RtmUpdateAndUnlockRoute function [RAS]","_rtmv2ref_rtmupdateandunlockroute","rras.rtmupdateandunlockroute","rtmv2/RtmUpdateAndUnlockRoute"]
old-location: rras\rtmupdateandunlockroute.htm
tech.root: RRAS
ms.assetid: 917e3e90-b06b-410d-8456-d76e2baa76f8
ms.date: 12/05/2018
ms.keywords: RtmUpdateAndUnlockRoute, RtmUpdateAndUnlockRoute function [RAS], _rtmv2ref_rtmupdateandunlockroute, rras.rtmupdateandunlockroute, rtmv2/RtmUpdateAndUnlockRoute
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
 - RtmUpdateAndUnlockRoute
 - rtmv2/RtmUpdateAndUnlockRoute
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
 - RtmUpdateAndUnlockRoute
---

# RtmUpdateAndUnlockRoute function


## -description

The 
<b>RtmUpdateAndUnlockRoute</b> function updates the position of the route in the set of routes for a destination, and adjusts the best route information for the destination.

This function is used after a client has locked a route and updated it directly (also known as <i>in-place updating</i>).

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteHandle [in]

Handle to the route to change.

### -param TimeToLive [in]

Specifies the time, in milliseconds, after which the route is expired. Specify INFINITE to prevent routes from expiring.

### -param RouteListHandle [in]

Handle to an optional route list to which to move the route. This parameter is optional and can be set to <b>NULL</b>.

### -param NotifyType [in]

Set this parameter to <b>NULL</b>. <i>NotifyType</i> is reserved for future use.

### -param NotifyHandle [in]

Set this parameter to <b>NULL</b>. <i>NotifyHandle</i> is reserved for future use.

### -param ChangeFlags [out]

Receives RTM_ROUTE_CHANGE_BEST if the best route was changed.

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
</table>

## -remarks

Before calling this function, the client should lock the route using 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>, which returns a pointer to the route. Then, the client can update the route information using the pointer. Finally, the client should call 
<b>RtmUpdateAndUnlockRoute</b>. If the function executes successfully, the route is unlocked. If the call failed, the client must unlock the route by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a> with the <i>LockRoute</i> parameter set to <b>FALSE</b>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/update-a-route-in-place-using-rtmupdateandunlockroute">Update a Route In Place Using RtmUpdateAndUnlockRoute</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutetodest">RtmDeleteRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetroutepointer">RtmGetRoutePointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmholddestination">RtmHoldDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>