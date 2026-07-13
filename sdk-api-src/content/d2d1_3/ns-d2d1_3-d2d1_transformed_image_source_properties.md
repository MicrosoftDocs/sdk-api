---
UID: NS:d2d1_3.D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
title: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES (d2d1_3.h)
description: Properties of a transformed image source.
helpviewer_keywords: ["D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES","D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure [Direct2D]","d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES","direct2d.d2d1_transformed_image_source_properties"]
old-location: direct2d\d2d1_transformed_image_source_properties.htm
tech.root: Direct2D
ms.assetid: E8A39769-07F2-42CA-A7CA-F83FF97E2076
ms.date: 12/05/2018
ms.keywords: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES, D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure [Direct2D], d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES, direct2d.d2d1_transformed_image_source_properties
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
 - d2d1_3/D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
---

# D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure


## -description

Properties of a transformed image source.

## -struct-fields

### -field orientation

Type: <b><a href="/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_orientation">D2D1_ORIENTATION</a></b>

The orientation at which the image source is drawn.

### -field scaleX

Type: <b>FLOAT</b>

The horizontal scale factor at which the image source is drawn.

### -field scaleY

Type: <b>FLOAT</b>

The vertical scale factor at which the image source is drawn.

### -field interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode used when the image source is drawn.  This is ignored if the image source is drawn using the DrawImage method, or using an image brush.

### -field options

Type: <b><a href="/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_transformed_image_source_options">D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS</a></b>

Image source option flags.