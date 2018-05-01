---
UID: NF:rtmv2.RtmDeleteRouteList
title: RtmDeleteRouteList function
author: windows-driver-content
description: The RtmDeleteRouteList function removes all routes from a client-specific route list, then frees any resources allocated to the list.
old-location: rras\rtmdeleteroutelist.htm
old-project: RRAS
ms.assetid: 0f8f04af-6ef6-42a7-a086-ba1706815ccb
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RtmDeleteRouteList, RtmDeleteRouteList function [RAS], _rtmv2ref_rtmdeleteroutelist, rras.rtmdeleteroutelist, rtmv2/RtmDeleteRouteList
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
-	RtmDeleteRouteList
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmDeleteRouteList function


## -description


The 
<b>RtmDeleteRouteList</b> function removes all routes from a client-specific route list, then frees any resources allocated to the list.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteListHandle [in]

Handle to the route list to delete.


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



This function also releases the handle to the route list.




## -see-also




<a href="https://msdn.microsoft.com/6fa732a8-6c2f-4034-ab13-d64845fab14c">RtmCreateRouteList</a>



<a href="https://msdn.microsoft.com/e0145bdc-5000-429d-8603-1ebc6003a2bc">RtmInsertInRouteList</a>
 

 

