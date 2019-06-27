---
UID: NF:rtmv2.RtmDeleteRouteList
title: RtmDeleteRouteList function (rtmv2.h)
author: windows-sdk-content
description: The RtmDeleteRouteList function removes all routes from a client-specific route list, then frees any resources allocated to the list.
old-location: rras\rtmdeleteroutelist.htm
tech.root: RRAS
ms.assetid: 0f8f04af-6ef6-42a7-a086-ba1706815ccb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmDeleteRouteList, RtmDeleteRouteList function [RAS], _rtmv2ref_rtmdeleteroutelist, rras.rtmdeleteroutelist, rtmv2/RtmDeleteRouteList
ms.topic: function
f1_keywords: 
 - "rtmv2/RtmDeleteRouteList"
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
 - RtmDeleteRouteList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtmDeleteRouteList function


## -description


The 
<b>RtmDeleteRouteList</b> function removes all routes from a client-specific route list, then frees any resources allocated to the list.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreateroutelist">RtmCreateRouteList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtminsertinroutelist">RtmInsertInRouteList</a>
 

 

