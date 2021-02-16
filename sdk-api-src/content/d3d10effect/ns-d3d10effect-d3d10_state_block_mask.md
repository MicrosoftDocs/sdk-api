---
UID: NS:d3d10effect._D3D10_STATE_BLOCK_MASK
title: D3D10_STATE_BLOCK_MASK (d3d10effect.h)
description: Indicates the device state.
helpviewer_keywords: ["D3D10_STATE_BLOCK_MASK","D3D10_STATE_BLOCK_MASK structure [Direct3D 10]","bf81f800-b1fd-0774-8da5-ae9bd9fc43d4","d3d10effect/D3D10_STATE_BLOCK_MASK","direct3d10.d3d10_state_block_mask"]
old-location: direct3d10\d3d10_state_block_mask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_state_block_mask.htm
ms.date: 12/05/2018
ms.keywords: D3D10_STATE_BLOCK_MASK, D3D10_STATE_BLOCK_MASK structure [Direct3D 10], bf81f800-b1fd-0774-8da5-ae9bd9fc43d4, d3d10effect/D3D10_STATE_BLOCK_MASK, direct3d10.d3d10_state_block_mask
req.header: d3d10effect.h
req.include-header: D3D10.h
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
req.typenames: D3D10_STATE_BLOCK_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_STATE_BLOCK_MASK
 - d3d10effect/_D3D10_STATE_BLOCK_MASK
 - D3D10_STATE_BLOCK_MASK
 - d3d10effect/D3D10_STATE_BLOCK_MASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_STATE_BLOCK_MASK
---

## -description

Indicates the device state.

## -struct-fields

### -field VS

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the vertex shader state.

### -field GS

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the geometry shader state.

### -field PS

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the pixel shader state.

### -field IAIndexBuffer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the index buffer state.

### -field IAInputLayout

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the input layout state.

### -field IAPrimitiveTopology

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the primitive topology state.

### -field OMRenderTargets

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the render targets states.

### -field OMDepthStencilState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the depth-stencil state.

### -field OMBlendState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the blend state.

### -field RSViewports

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the viewports states.

### -field RSScissorRects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the scissor rectangles states.

### -field RSRasterizerState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the rasterizer state.

### -field SOBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the stream-out buffers states.

### -field Predication

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Boolean value indicating whether to save the predication state.

### -field GSConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of geometry-shader constant buffers. The array is a multi-byte bitmask where each bit represents one buffer slot.

### -field GSSamplers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of geometry-shader samplers. The array is a multi-byte bitmask where each bit represents one sampler slot.

### -field GSShaderResources

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of geometry-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.

### -field IAVertexBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of vertex buffers. The array is a multi-byte bitmask where each bit represents one resource slot.

### -field PSConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of pixel-shader constant buffers. The array is a multi-byte bitmask where each bit represents one constant buffer slot.

### -field PSSamplers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of pixel-shader samplers. The array is a multi-byte bitmask where each bit represents one sampler slot.

### -field PSShaderResources

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of pixel-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.

### -field VSConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of vertex-shader constant buffers. The array is a multi-byte bitmask where each bit represents one constant buffer slot.

### -field VSSamplers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of vertex-shader samplers.  The array is a multi-byte bitmask where each bit represents one sampler slot.

### -field VSShaderResources

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Array of vertex-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.

## -remarks

A state-block mask indicates the device states that a pass or a technique changes.  The <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-d3d10stateblockmaskenablecapture">D3D10StateBlockMaskEnableCapture</a> function provides a convenient way of setting a range of bitmasks for the array members of <b>D3D10_STATE_BLOCK_MASK</b>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>