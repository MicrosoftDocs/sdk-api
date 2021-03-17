---
UID: NS:d3d11.D3D11_DEPTH_STENCILOP_DESC
title: D3D11_DEPTH_STENCILOP_DESC (d3d11.h)
description: Stencil operations that can be performed based on the results of stencil test.
helpviewer_keywords: ["D3D11_DEPTH_STENCILOP_DESC","D3D11_DEPTH_STENCILOP_DESC structure [Direct3D 11]","b5c19838-9f15-a711-8c15-008fbca8d2a1","d3d11/D3D11_DEPTH_STENCILOP_DESC","direct3d11.d3d11_depth_stencilop_desc"]
old-location: direct3d11\d3d11_depth_stencilop_desc.htm
tech.root: direct3d11
ms.assetid: 8c375d2f-ecec-4b9f-bd84-625dad53fa6a
ms.date: 12/05/2018
ms.keywords: D3D11_DEPTH_STENCILOP_DESC, D3D11_DEPTH_STENCILOP_DESC structure [Direct3D 11], b5c19838-9f15-a711-8c15-008fbca8d2a1, d3d11/D3D11_DEPTH_STENCILOP_DESC, direct3d11.d3d11_depth_stencilop_desc
req.header: d3d11.h
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
req.typenames: D3D11_DEPTH_STENCILOP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_DEPTH_STENCILOP_DESC
 - d3d11/D3D11_DEPTH_STENCILOP_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_DEPTH_STENCILOP_DESC
---

# D3D11_DEPTH_STENCILOP_DESC structure


## -description

Stencil operations that can be performed based on the results of stencil test.

## -struct-fields

### -field StencilFailOp

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_stencil_op">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing fails.

### -field StencilDepthFailOp

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_stencil_op">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing passes and depth testing fails.

### -field StencilPassOp

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_stencil_op">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing and depth testing both pass.

### -field StencilFunc

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_comparison_func">D3D11_COMPARISON_FUNC</a></b>

A function that compares stencil data against existing stencil data. The function options are listed in <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_comparison_func">D3D11_COMPARISON_FUNC</a>.

## -remarks

All stencil operations are specified as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_stencil_op">D3D11_STENCIL_OP</a>. The stencil operation can be set differently based on the outcome of the stencil test (which is referred to as <b>StencilFunc</b> in the stencil test portion of depth-stencil testing.

This structure is a member of a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">depth-stencil description</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>