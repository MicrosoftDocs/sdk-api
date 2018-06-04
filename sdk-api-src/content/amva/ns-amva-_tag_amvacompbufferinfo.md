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

# _tag_AMVACompBufferInfo structure


## -description



          The <b>AMVACompBufferInfo</b> structure describes the allocated surfaces and compressed buffer information.


## -struct-fields




### -field dwNumCompBuffers


            Number of buffers requested for compressed data.
          


### -field dwWidthToCreate


            Width of surface to create.
          


### -field dwHeightToCreate


            Height of surface to create.
          


### -field dwBytesToAllocate


            Total number of bytes used by each surface.
          


### -field ddCompCaps

<b>DDSCAPS2</b> structure defining the capabilities of the DirectDraw surface created to store compressed data.
          


### -field ddPixelFormat

<b>DDPIXELFORMAT</b> structure, describing the pixel format used to create surfaces to store compressed data.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/c32fb94d-396f-460a-9e69-1baaf14eff6e">IAMVideoAccelerator::GetCompBufferInfo</a>
 

 

