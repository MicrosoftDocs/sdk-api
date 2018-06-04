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

# D2D1_IMAGE_BRUSH_PROPERTIES structure


## -description


Describes image brush features.


## -struct-fields




### -field sourceRectangle

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The source rectangle in the image space from which the image will be tiled or interpolated.


### -field extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the image x-axis.


### -field extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the image y-axis.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use when scaling the image brush.


## -see-also




<a href="https://msdn.microsoft.com/f80947b7-7bd9-4097-8279-f70f5d92d5b6">ID2D1DeviceContext::CreateImageBrush</a>



<a href="https://msdn.microsoft.com/c5088ce2-5744-4061-957b-25831478a714">ID2D1ImageBrush</a>
 

 

