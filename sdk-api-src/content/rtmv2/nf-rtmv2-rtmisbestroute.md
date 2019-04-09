---
UID: NF:rtmv2.RtmIsBestRoute
title: RtmIsBestRoute function (rtmv2.h)
author: windows-sdk-content
description: The RtmIsBestRoute function returns the set of views in which the specified route is the best route to a destination.
old-location: rras\rtmisbestroute.htm
tech.root: RRAS
ms.assetid: 4c4b72a8-7a6c-4216-af2d-8dee55b910af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmIsBestRoute, RtmIsBestRoute function [RAS], _rtmv2ref_rtmisbestroute, rras.rtmisbestroute, rtmv2/RtmIsBestRoute
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
 - RtmIsBestRoute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmIsBestRoute function


## -description


The 
<b>RtmIsBestRoute</b> function returns the set of views in which the specified route is the best route to a destination.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteHandle [in]

Handle to the route to check.


### -param BestInViews [out]

Receives a pointer to the set of views for which the specified route is the best route.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a>



<a href="https://msdn.microsoft.com/5fc9cde7-9912-409f-85ee-c775b4d6ddc0">RtmGetExactMatchRoute</a>



<a href="https://msdn.microsoft.com/b6ff1b1f-fd0e-4cfb-9030-67e27e8578f6">RtmGetLessSpecificDestination</a>



<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a>
 

 

