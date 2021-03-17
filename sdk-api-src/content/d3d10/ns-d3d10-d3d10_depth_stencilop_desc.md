---
UID: NS:d3d10.D3D10_DEPTH_STENCILOP_DESC
title: D3D10_DEPTH_STENCILOP_DESC (d3d10.h)
description: Describes the stencil operations that can be performed based on the results of stencil test.
helpviewer_keywords: ["D3D10_DEPTH_STENCILOP_DESC","D3D10_DEPTH_STENCILOP_DESC structure [Direct3D 10]","d3d10/D3D10_DEPTH_STENCILOP_DESC","direct3d10.d3d10_depth_stencilop_desc","f40038a7-1ea3-7c24-dccb-e727b020078f"]
old-location: direct3d10\d3d10_depth_stencilop_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencilop_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_DEPTH_STENCILOP_DESC, D3D10_DEPTH_STENCILOP_DESC structure [Direct3D 10], d3d10/D3D10_DEPTH_STENCILOP_DESC, direct3d10.d3d10_depth_stencilop_desc, f40038a7-1ea3-7c24-dccb-e727b020078f
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
req.typenames: D3D10_DEPTH_STENCILOP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_DEPTH_STENCILOP_DESC
 - d3d10/D3D10_DEPTH_STENCILOP_DESC
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
 - D3D10_DEPTH_STENCILOP_DESC
---

# D3D10_DEPTH_STENCILOP_DESC structure


## -description

Describes the stencil operations that can be performed based on the results of <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">stencil test</a>.

## -struct-fields

### -field StencilFailOp

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing fails. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.

### -field StencilDepthFailOp

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing passes and depth testing fails. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.

### -field StencilPassOp

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_stencil_op">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing and depth testing both pass. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.

### -field StencilFunc

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a></b>

A member of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a> enumerated type that describes how stencil data is compared against existing stencil data. The default value is <b>D3D10_COMPARISON_ALWAYS</b>.

## -remarks

The stencil operation can be set differently based on the outcome of the stencil test by using the <b>StencilFunc</b> member.  This can be done for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">stencil test</a> portion of depth-stencil testing.

The D3D10_DEPTH_STENCILOP_DESC structure is a member of the <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_desc">D3D10_DEPTH_STENCIL_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>