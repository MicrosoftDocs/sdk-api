---
UID: NF:d2d1_1helper.ImageBrushProperties
title: ImageBrushProperties function
author: windows-sdk-content
description: Creates a D2D1_IMAGE_BRUSH_PROPERTIES structure.
old-location: direct2d\imagebrushproperties.htm
tech.root: Direct2D
ms.assetid: 824FA979-7D68-4383-BE3B-C3F39C1AAF77
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ImageBrushProperties, ImageBrushProperties function [Direct2D], d2d1_1helper/ImageBrushProperties, direct2d.imagebrushproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ImageBrushProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



