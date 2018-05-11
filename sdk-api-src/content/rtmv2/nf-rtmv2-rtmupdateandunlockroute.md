---
UID: NF:rtmv2.RtmUpdateAndUnlockRoute
title: RtmUpdateAndUnlockRoute function
author: windows-driver-content
description: The RtmUpdateAndUnlockRoute function updates the position of the route in the set of routes for a destination, and adjusts the best route information for the destination.
old-location: rras\rtmupdateandunlockroute.htm
old-project: RRAS
ms.assetid: 917e3e90-b06b-410d-8456-d76e2baa76f8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: RtmUpdateAndUnlockRoute, RtmUpdateAndUnlockRoute function [RAS], _rtmv2ref_rtmupdateandunlockroute, rras.rtmupdateandunlockroute, rtmv2/RtmUpdateAndUnlockRoute
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
-	RtmUpdateAndUnlockRoute
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmUpdateAndUnlockRoute function


## -description


The 
<b>RtmUpdateAndUnlockRoute</b> function updates the position of the route in the set of routes for a destination, and adjusts the best route information for the destination.

This function is used after a client has locked a route and updated it directly (also known as <i>in-place updating</i>).


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteHandle [in]

Handle to the route to change.


### -param TimeToLive [in]

Specifies the time, in milliseconds, after which the route is expired. Specify INFINITE to prevent routes from expiring.


### -param OPTIONAL

TBD


### -param NotifyType [in]

Set this parameter to <b>NULL</b>. <i>NotifyType</i> is reserved for future use.


### -param ChangeFlags [out]

Receives RTM_ROUTE_CHANGE_BEST if the best route was changed.


#### - NotifyHandle [in]

Set this parameter to <b>NULL</b>. <i>NotifyHandle</i> is reserved for future use.


#### - RouteListHandle [in]

Handle to an optional route list to which to move the route. This parameter is optional and can be set to <b>NULL</b>.


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
<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a>, which returns a pointer to the route. Then, the client can update the route information using the pointer. Finally, the client should call 
<b>RtmUpdateAndUnlockRoute</b>. If the function executes successfully, the route is unlocked. If the call failed, the client must unlock the route by calling 
<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a> with the <i>LockRoute</i> parameter set to <b>FALSE</b>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/3598a28f-8ade-4b3f-9d31-4f2c84df2dd6">Update a Route In Place Using RtmUpdateAndUnlockRoute</a>.




## -see-also




<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/d82e68b4-aff4-4872-b719-d9354f35024c">RtmDeleteRouteToDest</a>



<a href="https://msdn.microsoft.com/889e318c-b515-48bc-9117-83e8c1bb6f1a">RtmGetRoutePointer</a>



<a href="https://msdn.microsoft.com/433d6d97-9541-496a-8d10-2a2fc31d043d">RtmHoldDestination</a>



<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a>
 

 

