---
UID: NF:rtmv2.RtmGetRoutePointer
title: RtmGetRoutePointer function
author: windows-sdk-content
description: The RtmGetRoutePointer function obtains a direct pointer to a route that allows the owner of the route read access.
old-location: rras\rtmgetroutepointer.htm
tech.root: RRAS
ms.assetid: 889e318c-b515-48bc-9117-83e8c1bb6f1a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RtmGetRoutePointer, RtmGetRoutePointer function [RAS], _rtmv2ref_rtmgetroutepointer, rras.rtmgetroutepointer, rtmv2/RtmGetRoutePointer
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
 - RtmGetRoutePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmGetRoutePointer function


## -description


The 
<b>RtmGetRoutePointer</b> function obtains a direct pointer to a route that allows the owner of the route read access.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteHandle [in]

Handle to the route.


### -param RoutePointer [out]

On input, <i>RoutePointer</i> is a pointer to <b>NULL</b>. 




On output, <i>RoutePointer</i> receives a pointer to the route.


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



The pointer that was returned points to the public part of the route.




## -see-also




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/d82e68b4-aff4-4872-b719-d9354f35024c">RtmDeleteRouteToDest</a>



<a href="https://msdn.microsoft.com/433d6d97-9541-496a-8d10-2a2fc31d043d">RtmHoldDestination</a>



<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a>



<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a>
 

 

