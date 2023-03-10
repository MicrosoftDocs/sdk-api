---
UID: NF:rtmv2.RtmAddRouteToDest
title: RtmAddRouteToDest function (rtmv2.h)
description: The RtmAddRouteToDest function adds a new route to the routing table or updates an existing route in the routing table. If the best route changes, a change notification is generated.
helpviewer_keywords: ["RTM_ROUTE_CHANGE_BEST","RTM_ROUTE_CHANGE_FIRST","RTM_ROUTE_CHANGE_NEW","RtmAddRouteToDest","RtmAddRouteToDest function [RAS]","_rtmv2ref_rtmaddroutetodest","rras.rtmaddroutetodest","rtmv2/RtmAddRouteToDest"]
old-location: rras\rtmaddroutetodest.htm
tech.root: RRAS
ms.assetid: 422beb9b-b7e8-446f-8294-9f87a9f66f7a
ms.date: 12/05/2018
ms.keywords: RTM_ROUTE_CHANGE_BEST, RTM_ROUTE_CHANGE_FIRST, RTM_ROUTE_CHANGE_NEW, RtmAddRouteToDest, RtmAddRouteToDest function [RAS], _rtmv2ref_rtmaddroutetodest, rras.rtmaddroutetodest, rtmv2/RtmAddRouteToDest
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
 - RtmAddRouteToDest
 - rtmv2/RtmAddRouteToDest
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
 - RtmAddRouteToDest
---

# RtmAddRouteToDest function


## -description

The 
<b>RtmAddRouteToDest</b> function adds a new route to the routing table or updates an existing route in the routing table. If the best route changes, a change notification is generated.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteHandle [in, out]

If the client has a handle (updating a route): On input, <i>RouteHandle</i> is a pointer to the route handle. On output, <i>RouteHandle</i> is unchanged. 




If the client does not have a handle and a handle must be returned (client is adding or updating a route): On input, <i>RouteHandle</i> is a pointer to <b>NULL</b>. On output, <i>RouteHandle</i> receives a pointer to the route handle. The values in <i>RouteInfo</i> are used to identify the route to update.

If a handle does not need to be returned (client is adding or updating a route): On input, <i>RouteHandle</i> is <b>NULL</b>. The values in <i>RouteInfo</i> are used to identify the route to update.

### -param DestAddress [in]

Pointer to the destination network address to which the route is being added or updated.

### -param RouteInfo [in]

Pointer to the route information to add or update.

### -param TimeToLive [in]

Specifies the time, in milliseconds, after which the route is expired. Specify INFINITE to prevent routes from expiring.

### -param RouteListHandle [in]

Handle to a route list to which to move the route. This parameter is optional and can be set to <b>NULL</b>.

### -param NotifyType [in]

Set this parameter to <b>NULL</b>. This parameter is reserved for future use.

### -param NotifyHandle [in]

Set this parameter to <b>NULL</b>. This parameter is reserved for future use.

### -param ChangeFlags [in, out]

On input, <i>ChangeFlags</i> is a pointer to an <b>RTM_ROUTE_CHANGE_FLAGS</b> data type that  indicates whether the routing table manager should add a new route or update an existing one. 




On output, <i>ChangeFlags</i> is a pointer to an <b>RTM_ROUTE_CHANGE_FLAGS</b> data type that receives the flag indicating the type of change that was actually performed, and if the best route was changed. The following flags are used.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_CHANGE_FIRST"></a><a id="rtm_route_change_first"></a><dl>
<dt><b>RTM_ROUTE_CHANGE_FIRST</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the routing table manager should not check the <b>Neighbour</b> member of the <i>RouteInfo</i> parameter when determining if two routes are equal.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_CHANGE_NEW"></a><a id="rtm_route_change_new"></a><dl>
<dt><b>RTM_ROUTE_CHANGE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Returned by the routing table manager to indicate a new route was created.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_CHANGE_BEST"></a><a id="rtm_route_change_best"></a><dl>
<dt><b>RTM_ROUTE_CHANGE_BEST</b></dt>
</dl>
</td>
<td width="60%">
Returned by the routing table manager to indicate that the route that was added or updated was the best route, or that because of the change, a new route became the best route.

</td>
</tr>
</table>

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

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
</table>
 


<div> </div>

## -remarks

Two routes are considered equal if the following values are equal:

<ul>
<li>The destination network</li>
<li>The owner of the route</li>
<li>The neighbor that supplied the route</li>
</ul>
When a client is updating a route, it is more efficient to pass a handle to the route to update in the <i>RouteHandle</i> parameter, because the routing table manager does not have to perform a search for the route in the routing table.

If a handle was returned, release the handle when it is no longer required by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/add-and-update-routes-using-rtmaddroutetodest">Add and Update Routes Using RtmAddRouteToDest</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutetodest">RtmDeleteRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetroutepointer">RtmGetRoutePointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmholddestination">RtmHoldDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>