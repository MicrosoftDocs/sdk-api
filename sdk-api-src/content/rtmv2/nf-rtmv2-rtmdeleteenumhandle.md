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

# RtmDeleteEnumHandle function


## -description


The 
<b>RtmDeleteEnumHandle</b> function deletes the specified enumeration handle and frees all resources allocated for the enumeration.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EnumHandle [in]

Handle to be released. Any resources associated with the handle are also freed.


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




<a href="https://msdn.microsoft.com/6efea7b4-dd44-4b08-999d-62e7f660ed64">RtmCreateDestEnum</a>



<a href="https://msdn.microsoft.com/d26ce475-ea05-4e84-92da-06df9c386858">RtmCreateNextHopEnum</a>



<a href="https://msdn.microsoft.com/9d9c35e8-a9d4-4b30-a92c-f3188e11e317">RtmCreateRouteEnum</a>



<a href="https://msdn.microsoft.com/107fc253-58b3-479c-9cda-2c3b322e76f8">RtmCreateRouteListEnum</a>



<a href="https://msdn.microsoft.com/f793b54e-9591-4b9f-b109-8487013c7af5">RtmGetEnumDests</a>



<a href="https://msdn.microsoft.com/3e1a6064-6ba0-4ed8-b6df-1c347b098807">RtmGetEnumNextHops</a>



<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>



<a href="https://msdn.microsoft.com/eb338b7f-8461-4980-b92f-09d976661ff2">RtmReleaseDests</a>



<a href="https://msdn.microsoft.com/a21de428-7e9d-4596-a7ab-06a29b9852f7">RtmReleaseNextHops</a>



<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>
 

 

