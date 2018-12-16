---
UID: NF:rtmv2.RtmDeleteRouteToDest
title: RtmDeleteRouteToDest function
author: windows-sdk-content
description: The RtmDeleteRouteToDest function deletes a route from the routing table and updates the best-route information for the corresponding destination, if the best route changed. If the best route changes, a change notification is generated.
old-location: rras\rtmdeleteroutetodest.htm
tech.root: rras
ms.assetid: d82e68b4-aff4-4872-b719-d9354f35024c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmDeleteRouteToDest, RtmDeleteRouteToDest function [RAS], _rtmv2ref_rtmdeleteroutetodest, rras.rtmdeleteroutetodest, rtmv2/RtmDeleteRouteToDest
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
 - RtmDeleteRouteToDest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmDeleteRouteToDest function


## -description


The 
<b>RtmDeleteRouteToDest</b> function deletes a route from the routing table and updates the best-route information for the corresponding destination, if the best route changed. If the best route changes, a change notification is generated.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


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




<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/889e318c-b515-48bc-9117-83e8c1bb6f1a">RtmGetRoutePointer</a>



<a href="https://msdn.microsoft.com/433d6d97-9541-496a-8d10-2a2fc31d043d">RtmHoldDestination</a>



<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a>



<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a>
 

 

