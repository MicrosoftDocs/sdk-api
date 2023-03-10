---
UID: NS:d2d1_1.D2D1_LAYER_PARAMETERS1
title: D2D1_LAYER_PARAMETERS1 (d2d1_1.h)
description: Contains the content bounds, mask information, opacity settings, and other options for a layer resource. (D2D1_LAYER_PARAMETERS1)
helpviewer_keywords: ["D2D1_LAYER_PARAMETERS1","D2D1_LAYER_PARAMETERS1 structure [Direct2D]","d2d1_1/D2D1_LAYER_PARAMETERS1","direct2d.d2d1_layer_parameters1"]
old-location: direct2d\d2d1_layer_parameters1.htm
tech.root: Direct2D
ms.assetid: D7CC93F8-D871-4DFC-84A3-CA60EB52FF0A
ms.date: 12/05/2018
ms.keywords: D2D1_LAYER_PARAMETERS1, D2D1_LAYER_PARAMETERS1 structure [Direct2D], d2d1_1/D2D1_LAYER_PARAMETERS1, direct2d.d2d1_layer_parameters1
req.header: d2d1_1.h
req.include-header: D2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_LAYER_PARAMETERS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_LAYER_PARAMETERS1
 - d2d1_1/D2D1_LAYER_PARAMETERS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_LAYER_PARAMETERS1
---

# D2D1_LAYER_PARAMETERS1 structure


## -description

Contains the content bounds, mask information, opacity settings, and other options for a layer resource.

## -struct-fields

### -field contentBounds

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The content bounds of the layer. Content outside these bounds is not guaranteed to render.

### -field geometricMask

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometric mask specifies the area of the layer that is composited into the render target.

### -field maskAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the geometricMask.

### -field maskTransform

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer.

### -field opacity

Type: <b>FLOAT</b>

An opacity value that is applied uniformly to all resources in the layer when compositing to the target.

### -field opacityBrush

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

A brush that is used to modify the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.

### -field layerOptions

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1">D2D1_LAYER_OPTIONS1</a></b>

Additional options for the layer creation.

## -see-also

<a href="/windows/desktop/Direct2D/direct2d-layers-overview">Layers Overview</a>
