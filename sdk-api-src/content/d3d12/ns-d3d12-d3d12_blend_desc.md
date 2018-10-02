---
UID: NS:d3d12.D3D12_BLEND_DESC
title: D3D12_BLEND_DESC
author: windows-sdk-content
description: Describes the blend state.
old-location: direct3d12\d3d12_blend_desc.htm
tech.root: direct3d12
ms.assetid: FFCA10AF-1081-4D4B-900D-C3692D0B5A91
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_BLEND_DESC, D3D12_BLEND_DESC structure, d3d12/D3D12_BLEND_DESC, direct3d12.d3d12_blend_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_BLEND_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_BLEND_DESC
req.redist: 
---

# D3D12_BLEND_DESC structure


## -description


Describes the blend state.


## -struct-fields




### -field AlphaToCoverageEnable

Specifies whether to use alpha-to-coverage as a multisampling technique when setting a pixel to a render target. For more info about using alpha-to-coverage, see <a href="https://msdn.microsoft.com/en-us/library/Bb205072(v=VS.85).aspx">Alpha-To-Coverage</a>.
          


### -field IndependentBlendEnable

Specifies whether to enable independent blending in simultaneous render targets.  Set to <b>TRUE</b> to enable independent blending. If set to <b>FALSE</b>, only the <b>RenderTarget</b>[0] members are used; <b>RenderTarget</b>[1..7] are ignored.
          


### -field RenderTarget

An array of  <a href="https://msdn.microsoft.com/911158CF-5F4F-4211-8CC6-F73BDB697BC5">D3D12_RENDER_TARGET_BLEND_DESC</a> structures that describe the blend states for render targets; these correspond to the eight render targets
            that can be bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> at one time.
          


## -remarks



A <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a blend-state structure that controls blending by the output-merger stage.
      

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
 

When you set the <b>LogicOpEnable</b> member of the first element of the <b>RenderTarget</b> array (<b>RenderTarget</b>[0]) to <b>TRUE</b>, you must also set the <b>BlendEnable</b> member of  <b>RenderTarget</b>[0] to <b>FALSE</b>, and the <b>IndependentBlendEnable</b> member of  this structure to <b>FALSE</b>.  This reflects the limitation in hardware that you can't mix logic operations with blending across multiple render targets, and that when you use a logic operation, you must apply the same logic operation to all render targets.
        

Note the helper structure, <a href="https://msdn.microsoft.com/D37BB62E-904B-4953-9119-21F3B37570C0">CD3DX12_BLEND_DESC</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

