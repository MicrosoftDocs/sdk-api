---
UID: NF:d2d1_1helper.LayerParameters1
title: LayerParameters1 function (d2d1_1helper.h)
description: Returns a D2D1_LAYER_PARAMETERS1 struct that contains the content bounds, mask information, opacity settings, and other options for a layer resource.
helpviewer_keywords: ["LayerParameters1","LayerParameters1 function [Direct2D]","d2d1_1helper/LayerParameters1","direct2d.layerparameters1"]
old-location: direct2d\layerparameters1.htm
tech.root: Direct2D
ms.assetid: 8E882B23-CD6C-4CEB-9297-837B4E278BB7
ms.date: 12/05/2018
ms.keywords: LayerParameters1, LayerParameters1 function [Direct2D], d2d1_1helper/LayerParameters1, direct2d.layerparameters1
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
 - LayerParameters1
 - d2d1_1helper/LayerParameters1
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
 - LayerParameters1
---

# LayerParameters1 function


## -description

Returns a <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1">D2D1_LAYER_PARAMETERS1</a> struct that contains the content bounds, mask information, opacity settings, and other options for a layer resource.

## -parameters

### -param contentBounds [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The content bounds of the layer. Content outside these bounds is not guaranteed to render.

### -param geometricMask [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometric mask specifies the area of the layer that is composited into the render target.

### -param maskAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the geometricMask.

### -param maskTransform

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer.

### -param opacity

Type: <b>FLOAT</b>

An opacity value that is applied uniformly to all resources in the layer when compositing to the target.

### -param opacityBrush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

A brush that is used to modify the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.

### -param layerOptions

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1">D2D1_LAYER_OPTIONS1</a></b>

Additional options for the layer creation.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1">D2D1_LAYER_PARAMETERS1</a></b>

The filled layer parameters struct.