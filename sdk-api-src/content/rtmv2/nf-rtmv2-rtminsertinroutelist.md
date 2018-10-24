---
UID: NF:rtmv2.RtmInsertInRouteList
title: RtmInsertInRouteList function
author: windows-sdk-content
description: The RtmInsertInRouteList function inserts the specified set of routes into the client's route list. If a route is already in another list, the route is removed from the old list and inserted into the new one.
old-location: rras\rtminsertinroutelist.htm
tech.root: rras
ms.assetid: e0145bdc-5000-429d-8603-1ebc6003a2bc
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: RtmInsertInRouteList, RtmInsertInRouteList function [RAS], _rtmv2ref_rtminsertinroutelist, rras.rtminsertinroutelist, rtmv2/RtmInsertInRouteList
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
 - RtmInsertInRouteList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmInsertInRouteList function


## -description


The 
<b>RtmInsertInRouteList</b> function inserts the specified set of routes into the client's route list. If a route is already in another list, the route is removed from the old list and inserted into the new one.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param RouteListHandle [in]

Handle to the route list to which to add routes. Specify <b>NULL</b> to remove the specified routes from their old lists.


### -param NumRoutes [in]

Specifies the number of routes in <i>RouteHandles</i>.


### -param RouteHandles [in]

Pointer to an array of route handles to move from the old list to the new list.


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
 




## -remarks



When the routes are no longer required, release them by calling 
<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3">Use a Client-Specific Route List</a>.




## -see-also




<a href="https://msdn.microsoft.com/6fa732a8-6c2f-4034-ab13-d64845fab14c">RtmCreateRouteList</a>



<a href="https://msdn.microsoft.com/0f8f04af-6ef6-42a7-a086-ba1706815ccb">RtmDeleteRouteList</a>
 

 

