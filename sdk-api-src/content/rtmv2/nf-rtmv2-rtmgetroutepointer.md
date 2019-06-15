---
UID: NF:rtmv2.RtmGetRoutePointer
title: RtmGetRoutePointer function (rtmv2.h)
author: windows-sdk-content
description: The RtmGetRoutePointer function obtains a direct pointer to a route that allows the owner of the route read access.
old-location: rras\rtmgetroutepointer.htm
tech.root: RRAS
ms.assetid: 889e318c-b515-48bc-9117-83e8c1bb6f1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmGetRoutePointer, RtmGetRoutePointer function [RAS], _rtmv2ref_rtmgetroutepointer, rras.rtmgetroutepointer, rtmv2/RtmGetRoutePointer
ms.topic: function
f1_keywords: ["rtmv2/RtmGetRoutePointer"]
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
ms.custom: 19H1
---

# RtmGetRoutePointer function


## -description


The 
<b>RtmGetRoutePointer</b> function obtains a direct pointer to a route that allows the owner of the route read access.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-_rtm_route_info">RTM_ROUTE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutetodest">RtmDeleteRouteToDest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmholddestination">RtmHoldDestination</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmupdateandunlockroute">RtmUpdateAndUnlockRoute</a>
 

 

