---
UID: NF:rtmv2.RtmHoldDestination
title: RtmHoldDestination function (rtmv2.h)
description: The RtmHoldDestination function marks a destination to be put in the hold-down state for a certain amount of time. A hold down only happens if the last route for the destination in any view is deleted.
helpviewer_keywords: ["RtmHoldDestination","RtmHoldDestination function [RAS]","_rtmv2ref_rtmholddestination","rras.rtmholddestination","rtmv2/RtmHoldDestination"]
old-location: rras\rtmholddestination.htm
tech.root: RRAS
ms.assetid: 433d6d97-9541-496a-8d10-2a2fc31d043d
ms.date: 12/05/2018
ms.keywords: RtmHoldDestination, RtmHoldDestination function [RAS], _rtmv2ref_rtmholddestination, rras.rtmholddestination, rtmv2/RtmHoldDestination
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
 - RtmHoldDestination
 - rtmv2/RtmHoldDestination
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
 - RtmHoldDestination
---

# RtmHoldDestination function


## -description

The 
<b>RtmHoldDestination</b> function marks a destination to be put in the hold-down state for a certain amount of time. A hold down only happens if the last route for the destination in any view is deleted.

Routing protocols that use hold-down states continue to advertise the last route until the hold-down expires, even if newer routes arrive in the meantime. The route is advertised as a deleted route. The newer routes are, however, used by the routing protocols for forwarding purposes. New routes are advertised when the hold down expires.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestHandle [in]

Handle to the destination to mark for holding.

### -param TargetViews [in]

Specifies the views in which to hold the destination.

### -param HoldTime [in]

Specifies how long, in milliseconds, to hold the destination.

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
The hold time specified was zero.

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

All routes in a hold-down state are held for all views for a single, maximum hold-down time, regardless of the <i>HoldTime</i> specified.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/use-the-route-hold-down-state">Use the Route Hold-Down State</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutetodest">RtmDeleteRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>