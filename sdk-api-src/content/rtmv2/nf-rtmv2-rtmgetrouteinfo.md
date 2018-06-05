---
UID: NF:rtmv2.RtmGetRouteInfo
title: RtmGetRouteInfo function
author: windows-sdk-content
description: The RtmGetRouteInfo function returns information for the specified route.
old-location: rras\rtmgetrouteinfo.htm
old-project: RRAS
ms.assetid: 13fc70de-f6cd-4e7a-b79d-c2fe811e08a4
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RtmGetRouteInfo, RtmGetRouteInfo function [RAS], _rtmv2ref_rtmgetrouteinfo, rras.rtmgetrouteinfo, rtmv2/RtmGetRouteInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmGetRouteInfo
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RtmGetRouteInfo function


## -description


The 
<b>RtmGetRouteInfo</b> function returns information for the specified route.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteHandle [in]

Handle to the route to find.


### -param OPTIONAL

TBD




#### - DestAddress [out]

If a pointer must be returned: On input, <i>DestAddress</i> is a pointer to <b>NULL</b>. On output, <i>DestAddress</i> receives a pointer to the destination's 
<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a> structure; otherwise, <i>DestAddress</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>DestAddress</i> is <b>NULL</b>.


#### - RouteInfo [out]

If a pointer must be returned: On input, <i>RouteInfo</i> is a pointer to <b>NULL</b>. On output, <i>RouteInfo</i> receives a pointer to the route; otherwise, <i>RouteInfo</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>RouteInfo</i> is <b>NULL</b>.


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





## -remarks



When the routes are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/927d2a32-17bc-453c-b65b-144151bea902">RtmReleaseRouteInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/927d2a32-17bc-453c-b65b-144151bea902">RtmReleaseRouteInfo</a>
 

 

