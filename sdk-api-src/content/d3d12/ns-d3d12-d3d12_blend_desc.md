---
UID: NS:d3d12.D3D12_BLEND_DESC
title: D3D12_BLEND_DESC (d3d12.h)
description: Describes the blend state. (D3D12_BLEND_DESC)
helpviewer_keywords: ["D3D12_BLEND_DESC","D3D12_BLEND_DESC structure","d3d12/D3D12_BLEND_DESC","direct3d12.d3d12_blend_desc"]
old-location: direct3d12\d3d12_blend_desc.htm
tech.root: direct3d12
ms.assetid: FFCA10AF-1081-4D4B-900D-C3692D0B5A91
ms.date: 12/05/2018
ms.keywords: D3D12_BLEND_DESC, D3D12_BLEND_DESC structure, d3d12/D3D12_BLEND_DESC, direct3d12.d3d12_blend_desc
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
req.typenames: D3D12_BLEND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BLEND_DESC
 - d3d12/D3D12_BLEND_DESC
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
 - D3D12_BLEND_DESC
---

## -description

Describes the blend state.

## -struct-fields

### -field AlphaToCoverageEnable

Specifies whether to use alpha-to-coverage as a multisampling technique when setting a pixel to a render target. For more info about using alpha-to-coverage, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">Alpha-To-Coverage</a>.

### -field IndependentBlendEnable

Specifies whether to enable independent blending in simultaneous render targets. Set to <b>TRUE</b> to enable independent blending. If set to <b>FALSE</b>, only the <b>RenderTarget</b>[0] members are used; <b>RenderTarget</b>[1..7] are ignored.

See the **Remarks** section for restrictions.

### -field RenderTarget

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc">D3D12_RENDER_TARGET_BLEND_DESC</a> structures that describe the blend states for render targets; these correspond to the eight render targets that can be bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> at one time.

## -remarks

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a blend-state structure that controls blending by the output-merger stage.

Here are the default values for blend state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>AlphaToCoverageEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>IndependentBlendEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].BlendEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].LogicOpEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlend</td>
<td>D3D12_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlend</td>
<td>D3D12_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOp</td>
<td>D3D12_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlendAlpha</td>
<td>D3D12_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlendAlpha</td>
<td>D3D12_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOpAlpha</td>
<td>D3D12_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].LogicOp</td>
<td>D3D12_LOGIC_OP_NOOP</td>
</tr>
<tr>
<td>RenderTarget[0].RenderTargetWriteMask</td>
<td>D3D12_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>

When you set the <b>LogicOpEnable</b> member of the first element of the <b>RenderTarget</b> array (<b>RenderTarget</b>[0]) to <b>TRUE</b>, you must also set the <b>BlendEnable</b> member of <b>RenderTarget</b>[0] to <b>FALSE</b>, and the <b>IndependentBlendEnable</b> member of this structure to <b>FALSE</b>. This reflects the limitation in hardware that you can't mix logic operations with blending across multiple render targets, and that when you use a logic operation, you must apply the same logic operation to all render targets.

Note the helper structure, <a href="/windows/desktop/direct3d12/cd3dx12-blend-desc">CD3DX12_BLEND_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core structures</a>
