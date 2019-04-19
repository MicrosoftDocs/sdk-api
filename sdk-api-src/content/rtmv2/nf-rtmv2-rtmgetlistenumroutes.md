---
UID: NF:rtmv2.RtmGetListEnumRoutes
title: RtmGetListEnumRoutes function (rtmv2.h)
author: windows-sdk-content
description: The RtmGetListEnumRoutes function enumerates a set of routes in a specified route list.
old-location: rras\rtmgetlistenumroutes.htm
tech.root: RRAS
ms.assetid: 9ee40466-63e9-40c4-82bf-45f819d0ae58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmGetListEnumRoutes, RtmGetListEnumRoutes function [RAS], _rtmv2ref_rtmgetlistenumroutes, rras.rtmgetlistenumroutes, rtmv2/RtmGetListEnumRoutes
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
 - RtmGetListEnumRoutes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtmGetListEnumRoutes function


## -description


The 
<b>RtmGetListEnumRoutes</b> function enumerates a set of routes in a specified route list.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EnumHandle [in]

Handle to the route list to enumerate.


### -param NumRoutes [in, out]

On input, <i>NumRoutes</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of routes that can be received by <i>RouteHandles</i>. 




On output, <i>NumRoutes</i> receives the actual number of routes received by <i>RouteHandles</i>.


### -param RouteHandles [out]

On input, <i>DestInfo</i> is a pointer to an array of 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structures. 




On output, <i>DestInfo</i> is filled with the requested destination information.


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
</table>
 


<div> </div>





## -remarks



Call this function repeatedly to retrieve all routes.

There are no more routes to enumerate when the routing table manager returns zero in <i>NumRoutes</i>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3">Use a Client-Specific Route List</a>.




## -see-also




<a href="https://msdn.microsoft.com/107fc253-58b3-479c-9cda-2c3b322e76f8">RtmCreateRouteListEnum</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>
 

 

