---
UID: NS:d3d12.D3D12_RENDER_TARGET_BLEND_DESC
title: D3D12_RENDER_TARGET_BLEND_DESC
author: windows-sdk-content
description: Describes the blend state for a render target.
old-location: direct3d12\d3d12_render_target_blend_desc.htm
old-project: direct3d12
ms.assetid: 911158CF-5F4F-4211-8CC6-F73BDB697BC5
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_RENDER_TARGET_BLEND_DESC, D3D12_RENDER_TARGET_BLEND_DESC structure, d3d12/D3D12_RENDER_TARGET_BLEND_DESC, direct3d12.d3d12_render_target_blend_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_RENDER_TARGET_BLEND_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RENDER_TARGET_BLEND_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RENDER_TARGET_BLEND_DESC structure


## -description


Describes the blend state for a render target.


## -struct-fields




### -field BlendEnable

Specifies whether to enable (or disable) blending. Set to <b>TRUE</b> to enable blending.


### -field LogicOpEnable

Specifies whether to enable (or disable) a logical operation. Set to <b>TRUE</b> to enable a logical operation.


### -field SrcBlend

A <a href="https://msdn.microsoft.com/BA114E1C-0E0B-4260-ACED-0FF3D426C764">D3D12_BLEND</a>-typed value that specifies the operation to perform on the RGB value that the pixel shader outputs. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field DestBlend

A <a href="https://msdn.microsoft.com/BA114E1C-0E0B-4260-ACED-0FF3D426C764">D3D12_BLEND</a>-typed value that specifies the operation to perform on the current RGB value in the render target. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field BlendOp

A <a href="https://msdn.microsoft.com/2C36BFCB-2871-446F-8A79-3E963DB50795">D3D12_BLEND_OP</a>-typed value that defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field SrcBlendAlpha

A <a href="https://msdn.microsoft.com/BA114E1C-0E0B-4260-ACED-0FF3D426C764">D3D12_BLEND</a>-typed value that specifies the operation to perform on the alpha value that the pixel shader outputs. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field DestBlendAlpha

A <a href="https://msdn.microsoft.com/BA114E1C-0E0B-4260-ACED-0FF3D426C764">D3D12_BLEND</a>-typed value that specifies the operation to perform on the current alpha value in the render target. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field BlendOpAlpha

A <a href="https://msdn.microsoft.com/2C36BFCB-2871-446F-8A79-3E963DB50795">D3D12_BLEND_OP</a>-typed value that defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field LogicOp

A  <a href="https://msdn.microsoft.com/4F6BBCA8-6CF1-42BD-8B05-CD6D285CDFBF">D3D12_LOGIC_OP</a>-typed value that specifies the logical operation to configure for the render target.


### -field RenderTargetWriteMask

A combination of <a href="https://msdn.microsoft.com/BC07C5E7-CFEC-4902-9FB1-74A4396190BC">D3D12_COLOR_WRITE_ENABLE</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies a write mask.


## -remarks



You specify an array of <b>D3D12_RENDER_TARGET_BLEND_DESC</b> structures in the <b>RenderTarget</b> member of the <a href="https://msdn.microsoft.com/FFCA10AF-1081-4D4B-900D-C3692D0B5A91">D3D12_BLEND_DESC</a> structure to describe the blend states for render targets; you can bind up to eight render targets to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> at one time.

For info about how blending is done, see the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.

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




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

