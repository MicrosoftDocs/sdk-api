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

# ImageBrushProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6">D2D1_IMAGE_BRUSH_PROPERTIES</a> structure.


## -parameters




### -param sourceRectangle

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The source rectangle in the image space from which the image will be tiled or interpolated.


### -param extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the image x-axis.


### -param extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the image y-axis.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/7a32f551-afad-4eb2-953f-a9acc71d7776">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use when scaling the image brush.


## -returns



Type: <b><a href="https://msdn.microsoft.com/c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6">D2D1_IMAGE_BRUSH_PROPERTIES</a></b>

The struct that describes the image brush.



