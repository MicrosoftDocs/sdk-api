---
UID: NF:d2d1helper.LayerParameters
title: LayerParameters function (d2d1helper.h)
description: Creates a D2D1_LAYER_PARAMETERS structure.
helpviewer_keywords: ["LayerParameters","LayerParameters function [Direct2D]","d2d1helper/LayerParameters","direct2d.layerparameters"]
old-location: direct2d\layerparameters.htm
tech.root: Direct2D
ms.assetid: c6a9ebca-5d60-4013-b35b-547b7f4600da
ms.date: 12/05/2018
ms.keywords: LayerParameters, LayerParameters function [Direct2D], d2d1helper/LayerParameters, direct2d.layerparameters
req.header: d2d1helper.h
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
 - LayerParameters
 - d2d1helper/LayerParameters
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
 - LayerParameters
---

# LayerParameters function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS</a> structure.

## -parameters

### -param contentBounds [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The content bounds of the layer. Content outside these bounds is not guaranteed to render.  The default value is <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-infiniterect">D2D1::InfiniteRect</a>.

### -param geometricMask [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

A mask that specifies the area of the  layer that is composited into the render target, or <b>NULL</b>. The default value is <b>NULL</b>.

### -param maskAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the  geometric mask. The default value is   <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE_PER_PRIMITIVE</a>.

### -param maskTransform

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer. The default value is <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix">D2D1::IdentityMatrix</a>.

### -param opacity

Type: <b>FLOAT</b>

An opacity that is applied uniformly to all resources in the layer when compositing to the target. The default value is 1.0.

### -param opacityBrush

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

A brush that is used to alter the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied by the corresponding layer pixel.  The default value is <b>NULL</b>.

### -param layerOptions

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options">D2D1_LAYER_OPTIONS</a></b>

A value that specifies whether the layer intends to render text with ClearType antialiasing. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options">D2D1_LAYER_OPTIONS_NONE</a>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS</a></b>

A structure that contains the content bounds, mask information, opacity settings, and other options for a layer resource.

## -see-also

<a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a>



<a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options">D2D1_LAYER_OPTIONS</a>



<a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>



<a href="/windows/desktop/Direct2D/direct2d-layers-overview">Layers Overview</a>