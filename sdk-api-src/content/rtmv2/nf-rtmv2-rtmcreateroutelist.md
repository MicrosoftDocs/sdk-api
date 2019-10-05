---
UID: NF:rtmv2.RtmCreateRouteList
title: RtmCreateRouteList function (rtmv2.h)
author: windows-sdk-content
description: The RtmCreateRouteList function creates a list in which the caller can keep a copy of the routes it owns.
old-location: rras\rtmcreateroutelist.htm
tech.root: RRAS
ms.assetid: 6fa732a8-6c2f-4034-ab13-d64845fab14c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtmCreateRouteList, RtmCreateRouteList function [RAS], _rtmv2ref_rtmcreateroutelist, rras.rtmcreateroutelist, rtmv2/RtmCreateRouteList
ms.topic: function
f1_keywords: 
 - "rtmv2/RtmCreateRouteList"
dev_langs:
 - c++
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
 - RtmCreateRouteList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtmCreateRouteList function


## -description


The 
<b>RtmCreateRouteList</b> function creates a list in which the caller can keep a copy of the routes it owns.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.


### -param RouteListHandle [out]

On input, <i>RouteListHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RouteListHandle</i> receives a pointer to a handle to the new route list.


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



For sample code using this function, see 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/use-a-client-specific-route-list">Use a Client-Specific Route List</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutelist">RtmDeleteRouteList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtminsertinroutelist">RtmInsertInRouteList</a>
 

 

