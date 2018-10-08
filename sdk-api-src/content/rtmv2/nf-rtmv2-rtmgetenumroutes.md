---
UID: NF:rtmv2.RtmGetEnumRoutes
title: RtmGetEnumRoutes function
author: windows-sdk-content
description: The RtmGetEnumRoutes function retrieves the next set of routes in the specified enumeration.
old-location: rras\rtmgetenumroutes.htm
tech.root: rras
ms.assetid: fb3977ef-9edd-4653-b65c-b6d0fb66a785
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: RtmGetEnumRoutes, RtmGetEnumRoutes function [RAS], _rtmv2ref_rtmgetenumroutes, rras.rtmgetenumroutes, rtmv2/RtmGetEnumRoutes
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
 - RtmGetEnumRoutes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmGetEnumRoutes function


## -description


The 
<b>RtmGetEnumRoutes</b> function retrieves the next set of routes in the specified enumeration.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EnumHandle [in]

Handle to the route enumeration.


### -param NumRoutes [in, out]

On input, <i>NumRoutes</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of routes that can be received by <i>RouteHandles</i>. 




On output, <i>NumRoutes</i> receives the actual number of routes received by <i>RouteHandles</i>.


### -param RouteHandles [out]

On input, <i>RouteHandles</i> is a pointer to an 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure. 




On output, <i>RouteHandles</i> receives an array of handles to routes.


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
The value pointed to by <i>NumRoutes</i> is larger than the maximum number of routes a client is allowed to retrieve with one call. Check 
<a href="https://msdn.microsoft.com/26644a09-8d49-4c9f-a7cd-5edbf93e83d0">RTM_REGN_PROFILE</a> for the maximum number of routes that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more routes to enumerate.

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



When the routes are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/78a50e4a-f3c7-4a0d-a528-18d35b66369d">Enumerate All Routes</a>.




## -see-also




<a href="https://msdn.microsoft.com/9d9c35e8-a9d4-4b30-a92c-f3188e11e317">RtmCreateRouteEnum</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>
 

 

