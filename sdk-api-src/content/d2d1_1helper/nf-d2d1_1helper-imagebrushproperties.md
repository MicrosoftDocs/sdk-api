---
UID: NF:d2d1_1helper.ImageBrushProperties
title: ImageBrushProperties function (d2d1_1helper.h)
description: Creates a D2D1_IMAGE_BRUSH_PROPERTIES structure.
helpviewer_keywords: ["ImageBrushProperties","ImageBrushProperties function [Direct2D]","d2d1_1helper/ImageBrushProperties","direct2d.imagebrushproperties"]
old-location: direct2d\imagebrushproperties.htm
tech.root: Direct2D
ms.assetid: 824FA979-7D68-4383-BE3B-C3F39C1AAF77
ms.date: 12/05/2018
ms.keywords: ImageBrushProperties, ImageBrushProperties function [Direct2D], d2d1_1helper/ImageBrushProperties, direct2d.imagebrushproperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageBrushProperties
 - d2d1_1helper/ImageBrushProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ImageBrushProperties
---

# ImageBrushProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_image_brush_properties">D2D1_IMAGE_BRUSH_PROPERTIES</a> structure.

## -parameters

### -param sourceRectangle

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The source rectangle in the image space from which the image will be tiled or interpolated.

### -param extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the image x-axis.

### -param extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the image y-axis.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use when scaling the image brush.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_image_brush_properties">D2D1_IMAGE_BRUSH_PROPERTIES</a></b>

The struct that describes the image brush.