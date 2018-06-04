---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RtmInsertInRouteList function


## -description


The 
<b>RtmInsertInRouteList</b> function inserts the specified set of routes into the client's route list. If a route is already in another list, the route is removed from the old list and inserted into the new one.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param OPTIONAL

TBD


### -param NumRoutes [in]

Specifies the number of routes in <i>RouteHandles</i>.


### -param RouteHandles [in]

Pointer to an array of route handles to move from the old list to the new list.


#### - RouteListHandle [in]

Handle to the route list to which to add routes. Specify <b>NULL</b> to remove the specified routes from their old lists.


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
 

 

