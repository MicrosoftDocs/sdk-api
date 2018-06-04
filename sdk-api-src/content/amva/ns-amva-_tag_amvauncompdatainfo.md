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

# _tag_AMVAUncompDataInfo structure


## -description



          The <b>AMVAUncompDataInfo</b> structure specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.


## -struct-fields




### -field dwUncompWidth


            Width of the decoded, uncompressed data, in pixels.


### -field dwUncompHeight


            Height of the decoded, uncompressed data, in pixels.
          


### -field ddUncompPixelFormat


            
              A <b>DDPIXELFORMAT</b> structure that specifies the pixel format of the uncompressed data.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/c32fb94d-396f-460a-9e69-1baaf14eff6e">IAMVideoAccelerator::GetCompBufferInfo</a>
 

 

