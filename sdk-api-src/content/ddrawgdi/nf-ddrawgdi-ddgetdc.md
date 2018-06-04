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

# DdGetDC function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4">NtGdiDdGetDC</a> function and returns a Windows Graphics Device Interface (GDI) 
   device context (DC) that represents the Microsoft DirectDraw surface indicated.


<b>GdiEntry7</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the DirectDraw surface for which a DC is requested.


### -param pColorTable

Optional pointer to a 256-entry array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures. If the color table is null, and the surface and display mode are both 8 bits per pixel, the DC shares the color table of the device.


## -returns



If successful, this function returns a valid <b>HDC</b>; otherwise it returns <b>NULL</b>.




## -remarks



If both the surface and the current display mode are palletized at 8 bits per pixel, the DC can be given the special property that its color table is shared by the color table of the display device. Applications are advised to call <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a> instead, which provides the same functionality in a manner independent of the operating system.


The returned DC must be freed by a call to <a href="https://msdn.microsoft.com/98def2a1-878d-4776-a519-32cb70107338">NtGdiDdReleaseDC</a> or <b>GdiEntry8</b>.





## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

