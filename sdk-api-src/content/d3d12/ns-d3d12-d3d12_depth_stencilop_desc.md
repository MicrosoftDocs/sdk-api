---
UID: NS:d3d12.D3D12_DEPTH_STENCILOP_DESC
title: D3D12_DEPTH_STENCILOP_DESC (d3d12.h)
description: Describes stencil operations that can be performed based on the results of stencil test.
helpviewer_keywords: ["D3D12_DEPTH_STENCILOP_DESC","D3D12_DEPTH_STENCILOP_DESC structure","d3d12/D3D12_DEPTH_STENCILOP_DESC","direct3d12.d3d12_depth_stencilop_desc"]
old-location: direct3d12\d3d12_depth_stencilop_desc.htm
tech.root: direct3d12
ms.assetid: 1E72B486-98E1-4140-80E3-6DF95ECA82DB
ms.date: 12/05/2018
ms.keywords: D3D12_DEPTH_STENCILOP_DESC, D3D12_DEPTH_STENCILOP_DESC structure, d3d12/D3D12_DEPTH_STENCILOP_DESC, direct3d12.d3d12_depth_stencilop_desc
req.header: d3d12.h
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
req.typenames: D3D12_DEPTH_STENCILOP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEPTH_STENCILOP_DESC
 - d3d12/D3D12_DEPTH_STENCILOP_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DEPTH_STENCILOP_DESC
---

# D3D12_DEPTH_STENCILOP_DESC structure


## -description

Describes stencil operations that can be performed based on the results of stencil test.

## -struct-fields

### -field StencilFailOp

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing fails.

### -field StencilDepthFailOp

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing passes and depth testing fails.

### -field StencilPassOp

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing and depth testing both pass.

### -field StencilFunc

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func">D3D12_COMPARISON_FUNC</a>-typed value that identifies the function that compares stencil data against existing stencil data.

## -remarks

All stencil operations are specified as a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op">D3D12_STENCIL_OP</a>-typed value. Each stencil operation can be set differently based on the outcome of the stencil test, which is referred to as <b>StencilFunc</b>, in the stencil test portion of depth-stencil testing.

Members of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a> have this structure for their data type.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>