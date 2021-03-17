---
UID: NF:rtmv2.RtmDeleteRouteToDest
title: RtmDeleteRouteToDest function (rtmv2.h)
description: The RtmDeleteRouteToDest function deletes a route from the routing table and updates the best-route information for the corresponding destination, if the best route changed. If the best route changes, a change notification is generated.
helpviewer_keywords: ["RtmDeleteRouteToDest","RtmDeleteRouteToDest function [RAS]","_rtmv2ref_rtmdeleteroutetodest","rras.rtmdeleteroutetodest","rtmv2/RtmDeleteRouteToDest"]
old-location: rras\rtmdeleteroutetodest.htm
tech.root: RRAS
ms.assetid: d82e68b4-aff4-4872-b719-d9354f35024c
ms.date: 12/05/2018
ms.keywords: RtmDeleteRouteToDest, RtmDeleteRouteToDest function [RAS], _rtmv2ref_rtmdeleteroutetodest, rras.rtmdeleteroutetodest, rtmv2/RtmDeleteRouteToDest
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
 - RtmDeleteRouteToDest
 - rtmv2/RtmDeleteRouteToDest
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
 - RtmDeleteRouteToDest
---

# RtmDeleteRouteToDest function


## -description

The 
<b>RtmDeleteRouteToDest</b> function deletes a route from the routing table and updates the best-route information for the corresponding destination, if the best route changed. If the best route changes, a change notification is generated.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteHandle [in]

Handle to the route to delete.

### -param ChangeFlags [out]

On input, <i>ChangeFlags</i> is a pointer to <b>RTM_ROUTE_CHANGE_FLAGS</b> data type. 




On output, <i>ChangeFlags</i> receives RTM_ROUTE_CHANGE_BEST flag if the best route was changed.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified route was not found.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The <i>RouteHandle</i> should not subsequently be released by a client if the client has already called 
<b>RtmDeleteRouteToDest</b> using that handle. The 
<b>RtmDeleteRouteToDest</b> function deletes the route and releases the handle.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetroutepointer">RtmGetRoutePointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmholddestination">RtmHoldDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>