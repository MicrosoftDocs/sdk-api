---
UID: NF:rtmv2.RtmReleaseRouteInfo
title: RtmReleaseRouteInfo function
author: windows-sdk-content
description: The RtmReleaseRouteInfo function releases a route structure.
old-location: rras\rtmreleaserouteinfo.htm
tech.root: rras
ms.assetid: 927d2a32-17bc-453c-b65b-144151bea902
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: RtmReleaseRouteInfo, RtmReleaseRouteInfo function [RAS], _rtmv2ref_rtmreleaserouteinfo, rras.rtmreleaserouteinfo, rtmv2/RtmReleaseRouteInfo
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
 - RtmReleaseRouteInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmReleaseRouteInfo function


## -description


The 
<b>RtmReleaseRouteInfo</b> function releases a route structure.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteInfo [in]

Pointer to the 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure to release. The route was obtained with a previous call to 
<a href="https://msdn.microsoft.com/13fc70de-f6cd-4e7a-b79d-c2fe811e08a4">RtmGetRouteInfo</a>.


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




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/13fc70de-f6cd-4e7a-b79d-c2fe811e08a4">RtmGetRouteInfo</a>
 

 

