---
UID: NF:rtmv2.RtmHoldDestination
title: RtmHoldDestination function
author: windows-sdk-content
description: The RtmHoldDestination function marks a destination to be put in the hold-down state for a certain amount of time. A hold down only happens if the last route for the destination in any view is deleted.
old-location: rras\rtmholddestination.htm
old-project: RRAS
ms.assetid: 433d6d97-9541-496a-8d10-2a2fc31d043d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RtmHoldDestination, RtmHoldDestination function [RAS], _rtmv2ref_rtmholddestination, rras.rtmholddestination, rtmv2/RtmHoldDestination
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmHoldDestination
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: ADAM
---

# RtmHoldDestination function


## -description


The 
<b>RtmHoldDestination</b> function marks a destination to be put in the hold-down state for a certain amount of time. A hold down only happens if the last route for the destination in any view is deleted.

Routing protocols that use hold-down states continue to advertise the last route until the hold-down expires, even if newer routes arrive in the meantime. The route is advertised as a deleted route. The newer routes are, however, used by the routing protocols for forwarding purposes. New routes are advertised when the hold down expires.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


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
<a href="https://msdn.microsoft.com/bdc97fad-4805-4432-96ca-9225a51c92eb">Use the Route Hold-Down State</a>.




## -see-also




<a href="https://msdn.microsoft.com/422beb9b-b7e8-446f-8294-9f87a9f66f7a">RtmAddRouteToDest</a>



<a href="https://msdn.microsoft.com/d82e68b4-aff4-4872-b719-d9354f35024c">RtmDeleteRouteToDest</a>



<a href="https://msdn.microsoft.com/8de3e4e3-f3bc-4a98-8a11-cc5b4db9027f">RtmLockRoute</a>



<a href="https://msdn.microsoft.com/917e3e90-b06b-410d-8456-d76e2baa76f8">RtmUpdateAndUnlockRoute</a>
 

 

