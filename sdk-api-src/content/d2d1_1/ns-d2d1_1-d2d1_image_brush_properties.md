---
UID: NS:d2d1_1.D2D1_IMAGE_BRUSH_PROPERTIES
title: D2D1_IMAGE_BRUSH_PROPERTIES (d2d1_1.h)
description: Describes image brush features.
helpviewer_keywords: ["D2D1_IMAGE_BRUSH_PROPERTIES","D2D1_IMAGE_BRUSH_PROPERTIES structure [Direct2D]","PD2D1_IMAGE_BRUSH_PROPERTIES","PD2D1_IMAGE_BRUSH_PROPERTIES structure pointer [Direct2D]","d2d1_1/D2D1_IMAGE_BRUSH_PROPERTIES","d2d1_1/PD2D1_IMAGE_BRUSH_PROPERTIES","direct2d.d2d1_image_brush_properties"]
old-location: direct2d\d2d1_image_brush_properties.htm
tech.root: Direct2D
ms.assetid: c7bcae4d-cdef-4bfc-aa5a-68b85497a7f6
ms.date: 12/05/2018
ms.keywords: D2D1_IMAGE_BRUSH_PROPERTIES, D2D1_IMAGE_BRUSH_PROPERTIES structure [Direct2D], PD2D1_IMAGE_BRUSH_PROPERTIES, PD2D1_IMAGE_BRUSH_PROPERTIES structure pointer [Direct2D], d2d1_1/D2D1_IMAGE_BRUSH_PROPERTIES, d2d1_1/PD2D1_IMAGE_BRUSH_PROPERTIES, direct2d.d2d1_image_brush_properties
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
targetos: Windows
req.typenames: D2D1_IMAGE_BRUSH_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_IMAGE_BRUSH_PROPERTIES
 - d2d1_1/D2D1_IMAGE_BRUSH_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_IMAGE_BRUSH_PROPERTIES
---

# D2D1_IMAGE_BRUSH_PROPERTIES structure


## -description

Describes image brush features.

## -struct-fields

### -field sourceRectangle

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The source rectangle in the image space from which the image will be tiled or interpolated.

### -field extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the image x-axis.

### -field extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the image y-axis.

### -field interpolationMode

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use when scaling the image brush.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createimagebrush(id2d1image_constd2d1_image_brush_properties__constd2d1_brush_properties__id2d1imagebrush)">ID2D1DeviceContext::CreateImageBrush</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1imagebrush">ID2D1ImageBrush</a>