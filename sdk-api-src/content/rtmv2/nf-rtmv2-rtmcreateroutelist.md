---
UID: NF:rtmv2.RtmCreateRouteList
title: RtmCreateRouteList function
author: windows-sdk-content
description: The RtmCreateRouteList function creates a list in which the caller can keep a copy of the routes it owns.
old-location: rras\rtmcreateroutelist.htm
tech.root: rras
ms.assetid: 6fa732a8-6c2f-4034-ab13-d64845fab14c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtmCreateRouteList, RtmCreateRouteList function [RAS], _rtmv2ref_rtmcreateroutelist, rras.rtmcreateroutelist, rtmv2/RtmCreateRouteList
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
 - RtmCreateRouteList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmCreateRouteList function


## -description


The 
<b>RtmCreateRouteList</b> function creates a list in which the caller can keep a copy of the routes it owns.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


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
<a href="https://msdn.microsoft.com/aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3">Use a Client-Specific Route List</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f8f04af-6ef6-42a7-a086-ba1706815ccb">RtmDeleteRouteList</a>



<a href="https://msdn.microsoft.com/e0145bdc-5000-429d-8603-1ebc6003a2bc">RtmInsertInRouteList</a>
 

 

