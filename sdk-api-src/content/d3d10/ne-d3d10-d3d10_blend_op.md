---
UID: NE:d3d10.D3D10_BLEND_OP
title: D3D10_BLEND_OP (d3d10.h)
description: RGB or alpha blending operation. (D3D10_BLEND_OP)
helpviewer_keywords: ["9bbf55a2-225d-7084-43ca-8305b06faa0d","D3D10_BLEND_OP","D3D10_BLEND_OP enumeration [Direct3D 10]","D3D10_BLEND_OP_ADD","D3D10_BLEND_OP_MAX","D3D10_BLEND_OP_MIN","D3D10_BLEND_OP_REV_SUBTRACT","D3D10_BLEND_OP_SUBTRACT","d3d10/D3D10_BLEND_OP","d3d10/D3D10_BLEND_OP_ADD","d3d10/D3D10_BLEND_OP_MAX","d3d10/D3D10_BLEND_OP_MIN","d3d10/D3D10_BLEND_OP_REV_SUBTRACT","d3d10/D3D10_BLEND_OP_SUBTRACT","direct3d10.d3d10_blend_op"]
old-location: direct3d10\d3d10_blend_op.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend_op.htm
ms.date: 12/05/2018
ms.keywords: 9bbf55a2-225d-7084-43ca-8305b06faa0d, D3D10_BLEND_OP, D3D10_BLEND_OP enumeration [Direct3D 10], D3D10_BLEND_OP_ADD, D3D10_BLEND_OP_MAX, D3D10_BLEND_OP_MIN, D3D10_BLEND_OP_REV_SUBTRACT, D3D10_BLEND_OP_SUBTRACT, d3d10/D3D10_BLEND_OP, d3d10/D3D10_BLEND_OP_ADD, d3d10/D3D10_BLEND_OP_MAX, d3d10/D3D10_BLEND_OP_MIN, d3d10/D3D10_BLEND_OP_REV_SUBTRACT, d3d10/D3D10_BLEND_OP_SUBTRACT, direct3d10.d3d10_blend_op
req.header: d3d10.h
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
req.typenames: D3D10_BLEND_OP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BLEND_OP
 - d3d10/D3D10_BLEND_OP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BLEND_OP
---

# D3D10_BLEND_OP enumeration


## -description

RGB or alpha blending operation.

## -enum-fields

### -field D3D10_BLEND_OP_ADD:1

Add source 1 and source 2.

### -field D3D10_BLEND_OP_SUBTRACT:2

Subtract source 1 from source 2.

### -field D3D10_BLEND_OP_REV_SUBTRACT:3

Subtract source 2 from source 1.

### -field D3D10_BLEND_OP_MIN:4

Find the minimum of source 1 and source 2.

### -field D3D10_BLEND_OP_MAX:5

Find the maximum of source 1 and source 2.

## -remarks

The runtime implements RGB blending and alpha blending separately. Therefore, blend state requires separate blend operations for RGB data and alpha data. These blend operations are specified in a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">blend description</a>. The two sources — source 1 and source 2 — are shown in the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">blending block diagram</a>.

Blend state is used by the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <b>blend operation</b> controls how the blending stage mathematically combines these modulated values.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
