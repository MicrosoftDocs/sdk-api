---
UID: NF:rtmv2.RtmReleaseRoutes
title: RtmReleaseRoutes function
author: windows-driver-content
description: The RtmReleaseRoutes function releases the route handles.
old-location: rras\rtmreleaseroutes.htm
old-project: RRAS
ms.assetid: 4c893144-a2c5-4dc8-83c1-cae0d3024505
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RtmReleaseRoutes, RtmReleaseRoutes function [RAS], _rtmv2ref_rtmreleaseroutes, rras.rtmreleaseroutes, rtmv2/RtmReleaseRoutes
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
-	RtmReleaseRoutes
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmReleaseRoutes function


## -description


The 
<b>RtmReleaseRoutes</b> function releases the route handles.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param NumRoutes [in]

Specifies the number of routes in <i>RouteHandles</i>.


### -param RouteHandles [in]

Pointer to an array of route handles to release. The handles were obtained with a previous call to 
<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>.


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




<a href="https://msdn.microsoft.com/9d9c35e8-a9d4-4b30-a92c-f3188e11e317">RtmCreateRouteEnum</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>
 

 

