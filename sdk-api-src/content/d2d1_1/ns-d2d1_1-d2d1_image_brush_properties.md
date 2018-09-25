---
UID: NS:d2d1_1.D2D1_IMAGE_BRUSH_PROPERTIES
title: D2D1_IMAGE_BRUSH_PROPERTIES
author: windows-sdk-content
description: Describes image brush features.
old-location: direct2d\d2d1_image_brush_properties.htm
tech.root: direct2d
ms.assetid: c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: D2D1_IMAGE_BRUSH_PROPERTIES, D2D1_IMAGE_BRUSH_PROPERTIES structure [Direct2D], PD2D1_IMAGE_BRUSH_PROPERTIES, PD2D1_IMAGE_BRUSH_PROPERTIES structure pointer [Direct2D], d2d1_1/D2D1_IMAGE_BRUSH_PROPERTIES, d2d1_1/PD2D1_IMAGE_BRUSH_PROPERTIES, direct2d.d2d1_image_brush_properties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_IMAGE_BRUSH_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_IMAGE_BRUSH_PROPERTIES
req.redist: 
---

# D2D1_IMAGE_BRUSH_PROPERTIES structure


## -description


Describes image brush features.


## -struct-fields




### -field sourceRectangle

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368151(v=VS.85).aspx">D2D1_RECT_F</a></b>

The source rectangle in the image space from which the image will be tiled or interpolated.


### -field extendModeX

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368100(v=VS.85).aspx">D2D1_EXTEND_MODE</a></b>

The extend mode in the image x-axis.


### -field extendModeY

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368100(v=VS.85).aspx">D2D1_EXTEND_MODE</a></b>

The extend mode in the image y-axis.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368151(v=VS.85).aspx">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use when scaling the image brush.


## -see-also




<a href="https://msdn.microsoft.com/f80947b7-7bd9-4097-8279-f70f5d92d5b6">ID2D1DeviceContext::CreateImageBrush</a>



<a href="https://msdn.microsoft.com/c5088ce2-5744-4061-957b-25831478a714">ID2D1ImageBrush</a>
 

 

