---
UID: NS:d3d12.D3D12_RENDER_TARGET_BLEND_DESC
title: D3D12_RENDER_TARGET_BLEND_DESC (d3d12.h)
description: Describes the blend state for a render target. (D3D12_RENDER_TARGET_BLEND_DESC)
helpviewer_keywords: ["D3D12_RENDER_TARGET_BLEND_DESC","D3D12_RENDER_TARGET_BLEND_DESC structure","d3d12/D3D12_RENDER_TARGET_BLEND_DESC","direct3d12.d3d12_render_target_blend_desc"]
old-location: direct3d12\d3d12_render_target_blend_desc.htm
tech.root: direct3d12
ms.assetid: 911158CF-5F4F-4211-8CC6-F73BDB697BC5
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_TARGET_BLEND_DESC, D3D12_RENDER_TARGET_BLEND_DESC structure, d3d12/D3D12_RENDER_TARGET_BLEND_DESC, direct3d12.d3d12_render_target_blend_desc
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
req.typenames: D3D12_RENDER_TARGET_BLEND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_TARGET_BLEND_DESC
 - d3d12/D3D12_RENDER_TARGET_BLEND_DESC
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
 - D3D12_RENDER_TARGET_BLEND_DESC
---

## -description

Describes the blend state for a render target.

## -struct-fields

### -field BlendEnable

Specifies whether to enable (or disable) blending. Set to <b>TRUE</b> to enable blending.

> [!NOTE]
> It's not valid for *LogicOpEnable* and *BlendEnable* to both be **TRUE**.

### -field LogicOpEnable

Specifies whether to enable (or disable) a logical operation. Set to <b>TRUE</b> to enable a logical operation.

> [!NOTE]
> It's not valid for *LogicOpEnable* and *BlendEnable* to both be **TRUE**.

### -field SrcBlend

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend">D3D12_BLEND</a>-typed value that specifies the operation to perform on the RGB value that the pixel shader outputs. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.

### -field DestBlend

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend">D3D12_BLEND</a>-typed value that specifies the operation to perform on the current RGB value in the render target. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.

### -field BlendOp

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op">D3D12_BLEND_OP</a>-typed value that defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.

### -field SrcBlendAlpha

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend">D3D12_BLEND</a>-typed value that specifies the operation to perform on the alpha value that the pixel shader outputs. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.

### -field DestBlendAlpha

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend">D3D12_BLEND</a>-typed value that specifies the operation to perform on the current alpha value in the render target. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.

### -field BlendOpAlpha

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op">D3D12_BLEND_OP</a>-typed value that defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.

### -field LogicOp

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op">D3D12_LOGIC_OP</a>-typed value that specifies the logical operation to configure for the render target.

### -field RenderTargetWriteMask

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable">D3D12_COLOR_WRITE_ENABLE</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies a write mask.

## -remarks

> [!NOTE]
> It's not valid for *LogicOpEnable* and *BlendEnable* to both be **TRUE**.

You specify an array of <b>D3D12_RENDER_TARGET_BLEND_DESC</b> structures in the <b>RenderTarget</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc">D3D12_BLEND_DESC</a> structure to describe the blend states for render targets; you can bind up to eight render targets to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> at one time.

For info about how blending is done, see the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

Here are the default values for blend state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>BlendEnable</td>
<td>FALSE</td>
</tr>
<tr>
<td>LogicOpEnable</td>
<td>FALSE</td>
</tr>
<tr>
<td>SrcBlend</td>
<td>D3D12_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlend</td>
<td>D3D12_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOp</td>
<td>D3D12_BLEND_OP_ADD</td>
</tr>
<tr>
<td>SrcBlendAlpha</td>
<td>D3D12_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlendAlpha</td>
<td>D3D12_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOpAlpha</td>
<td>D3D12_BLEND_OP_ADD</td>
</tr>
<tr>
<td>LogicOp</td>
<td>D3D12_LOGIC_OP_NOOP</td>
</tr>
<tr>
<td>RenderTargetWriteMask</td>
<td>D3D12_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
