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

# D3D11_VIDEO_COLOR structure


## -description


Defines a color value for Microsoft Direct3D 11 video.


## -struct-fields




### -field YCbCr

A <a href="https://msdn.microsoft.com/242D6032-62E5-4915-B074-6E595A12F912">D3D11_VIDEO_COLOR_YCbCrA</a> structure that contains a YCbCr color value.




### -field RGBA

A <a href="https://msdn.microsoft.com/DDD587DC-BB17-407D-9E9E-47015950A504">D3D11_VIDEO_COLOR_RGBA</a> structure that contains an RGB color value.




## -remarks



The anonymous union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.






## -see-also




<a href="https://msdn.microsoft.com/089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1">About YUV Video</a>



<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

