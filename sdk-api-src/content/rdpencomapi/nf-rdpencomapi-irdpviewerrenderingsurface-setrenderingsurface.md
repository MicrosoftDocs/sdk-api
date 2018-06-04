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

# IRDPViewerRenderingSurface::SetRenderingSurface


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/24d818ec-f58d-4bf1-adf8-c15560595147">IRDPViewerRenderingSurface</a> interface is no longer available for use as of Windows 10, version 1709.]

Sets the rendering surface to be used by the viewer.


## -parameters




### -param pRenderingSurface [in]

The address of the <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> object to use for the rendering surface.


### -param surfaceWidth [in]

The width, in pixels, of the rendering surface.


### -param surfaceHeight [in]

The height, in pixels, of the rendering surface.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/24d818ec-f58d-4bf1-adf8-c15560595147">IRDPViewerRenderingSurface</a>
 

 

