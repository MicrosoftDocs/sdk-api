---
UID: NS:d2d1.D2D1_LAYER_PARAMETERS
title: D2D1_LAYER_PARAMETERS (d2d1.h)
description: Contains the content bounds, mask information, opacity settings, and other options for a layer resource. (D2D1_LAYER_PARAMETERS)
helpviewer_keywords: ["D2D1_LAYER_PARAMETERS","D2D1_LAYER_PARAMETERS structure [Direct2D]","d2d1/D2D1_LAYER_PARAMETERS","direct2d.D2D1_LAYER_PARAMETERS"]
old-location: direct2d\D2D1_LAYER_PARAMETERS.htm
tech.root: Direct2D
ms.assetid: ce575df6-9464-4672-9a0e-ff7e016d9354
ms.date: 12/05/2018
ms.keywords: D2D1_LAYER_PARAMETERS, D2D1_LAYER_PARAMETERS structure [Direct2D], d2d1/D2D1_LAYER_PARAMETERS, direct2d.D2D1_LAYER_PARAMETERS
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_LAYER_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_LAYER_PARAMETERS
 - d2d1/D2D1_LAYER_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_LAYER_PARAMETERS
---

# D2D1_LAYER_PARAMETERS structure


## -description

Contains the content bounds, mask information, opacity settings, and other options for a layer resource.

## -struct-fields

### -field contentBounds

Type: <b><a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The content bounds of the layer. Content won't render outside these bounds.

### -field geometricMask

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometric mask specifies the area of the layer that is composited into the render target.

### -field maskAntialiasMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the geometricMask.

### -field maskTransform

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer.

### -field opacity

Type: <b>FLOAT</b>

An opacity value that is applied uniformly to all resources in the layer when compositing to the target.

### -field opacityBrush

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

A brush that is used to modify the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.

### -field layerOptions

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_layer_options">D2D1_LAYER_OPTIONS</a></b>

A value that specifies whether the layer intends to render text with ClearType antialiasing.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-layers-overview">Layers Overview</a>

