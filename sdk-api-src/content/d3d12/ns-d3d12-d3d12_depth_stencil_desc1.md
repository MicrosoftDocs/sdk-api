---
UID: NS:d3d12.D3D12_DEPTH_STENCIL_DESC1
title: D3D12_DEPTH_STENCIL_DESC1 (d3d12.h)
description: Describes depth-stencil state. (D3D12_DEPTH_STENCIL_DESC1)
helpviewer_keywords: ["D3D12_DEPTH_STENCIL_DESC1","D3D12_DEPTH_STENCIL_DESC1 structure","d3d12/D3D12_DEPTH_STENCIL_DESC1","direct3d12.d3d12_depth_stencil_desc1"]
old-location: direct3d12\d3d12_depth_stencil_desc1.htm
tech.root: direct3d12
ms.assetid: 0DDDC3BA-0DA5-4DA2-A265-1ABB85596132
ms.date: 12/05/2018
ms.keywords: D3D12_DEPTH_STENCIL_DESC1, D3D12_DEPTH_STENCIL_DESC1 structure, d3d12/D3D12_DEPTH_STENCIL_DESC1, direct3d12.d3d12_depth_stencil_desc1
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
req.typenames: D3D12_DEPTH_STENCIL_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEPTH_STENCIL_DESC1
 - d3d12/D3D12_DEPTH_STENCIL_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DEPTH_STENCIL_DESC1
---

# D3D12_DEPTH_STENCIL_DESC1 structure


## -description

Describes depth-stencil state.

## -struct-fields

### -field DepthEnable

Specifies whether to enable depth testing. Set this member to <b>TRUE</b> to enable depth testing.

### -field DepthWriteMask

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask">D3D12_DEPTH_WRITE_MASK</a>-typed value that identifies a portion of the depth-stencil buffer that can be modified by depth data.

### -field DepthFunc

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func">D3D12_COMPARISON_FUNC</a>-typed value that identifies a function that compares depth data against existing depth data.

### -field StencilEnable

Specifies whether to enable stencil testing. Set this member to <b>TRUE</b> to enable stencil testing.

### -field StencilReadMask

Identify a portion of the depth-stencil buffer for reading stencil data.

### -field StencilWriteMask

Identify a portion of the depth-stencil buffer for writing stencil data.

### -field FrontFace

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc">D3D12_DEPTH_STENCILOP_DESC</a> structure that describes how to use the results of the depth test and the stencil test for pixels whose surface normal is facing towards the camera.

### -field BackFace

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc">D3D12_DEPTH_STENCILOP_DESC</a> structure that describes how to use the results of the depth test and the stencil test for pixels whose surface normal is facing away from the camera.

### -field DepthBoundsTestEnable

TRUE to enable depth-bounds testing; otherwise, FALSE. The default value is FALSE.

## -remarks

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a depth-stencil-state structure that controls how depth-stencil testing is performed by the output-merger stage.

This table shows the default values of depth-stencil states.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>DepthEnable</td>
<td>TRUE</td>
</tr>
<tr>
<td>DepthWriteMask</td>
<td>D3D12_DEPTH_WRITE_MASK_ALL</td>
</tr>
<tr>
<td>DepthFunc</td>
<td>D3D12_COMPARISON_LESS</td>
</tr>
<tr>
<td>StencilEnable</td>
<td>FALSE</td>
</tr>
<tr>
<td>StencilReadMask</td>
<td>D3D12_DEFAULT_STENCIL_READ_MASK</td>
</tr>
<tr>
<td>StencilWriteMask</td>
<td>D3D12_DEFAULT_STENCIL_WRITE_MASK</td>
</tr>
<tr>
<td>
FrontFace.StencilFunc

and

BackFace.StencilFunc

</td>
<td>D3D12_COMPARISON_ALWAYS</td>
</tr>
<tr>
<td>
FrontFace.StencilDepthFailOp

and

BackFace.StencilDepthFailOp

</td>
<td>D3D12_STENCIL_OP_KEEP</td>
</tr>
<tr>
<td>
FrontFace.StencilPassOp

and

BackFace.StencilPassOp

</td>
<td>D3D12_STENCIL_OP_KEEP</td>
</tr>
<tr>
<td>
FrontFace.StencilFailOp

and

BackFace.StencilFailOp

</td>
<td>D3D12_STENCIL_OP_KEEP</td>
</tr>
<tr>
<td>DepthBoundsTestEnable</td>
<td>FALSE</td>
</tr>
</table>
 

The formats that support stenciling are DXGI_FORMAT_D24_UNORM_S8_UINT and DXGI_FORMAT_D32_FLOAT_S8X24_UINT.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
