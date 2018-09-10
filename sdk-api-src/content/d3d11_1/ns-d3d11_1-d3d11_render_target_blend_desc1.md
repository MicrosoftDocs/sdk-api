---
UID: NS:d3d11_1.D3D11_RENDER_TARGET_BLEND_DESC1
title: D3D11_RENDER_TARGET_BLEND_DESC1
author: windows-sdk-content
description: Describes the blend state for a render target.
old-location: direct3d11\d3d11_render_target_blend_desc1.htm
tech.root: direct3d11
ms.assetid: A8323E69-F385-4E91-8B1F-A7CD3D508A09
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D11_RENDER_TARGET_BLEND_DESC1, D3D11_RENDER_TARGET_BLEND_DESC1 structure [Direct3D 11], d3d11_1/D3D11_RENDER_TARGET_BLEND_DESC1, direct3d11.d3d11_render_target_blend_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - D3D11_1.h
api_name:
 - D3D11_RENDER_TARGET_BLEND_DESC1
product: Windows
targetos: Windows
req.typenames: D3D11_RENDER_TARGET_BLEND_DESC1
req.redist: 
---

# D3D11_RENDER_TARGET_BLEND_DESC1 structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes the blend state for a render target.


## -struct-fields




### -field BlendEnable

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Enable (or disable) blending.


### -field LogicOpEnable

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Enable (or disable) a logical operation.


### -field SrcBlend

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">D3D11_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">blend option</a> specifies the operation to perform on the RGB value that the pixel shader outputs. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field DestBlend

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">D3D11_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">blend option</a> specifies the operation to perform on the current RGB value in the render target. The <b>BlendOp</b> member defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field BlendOp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476088(v=VS.85).aspx">D3D11_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476088(v=VS.85).aspx">blend operation</a> defines how to combine the <b>SrcBlend</b> and <b>DestBlend</b> operations.


### -field SrcBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">D3D11_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">blend option</a> specifies the operation to perform on the alpha value that the pixel shader outputs. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field DestBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">D3D11_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476086(v=VS.85).aspx">blend option</a> specifies the operation to perform on the current alpha value in the render target. Blend options that end in _COLOR are not allowed. The <b>BlendOpAlpha</b> member defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field BlendOpAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476088(v=VS.85).aspx">D3D11_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Ff476088(v=VS.85).aspx">blend operation</a> defines how to combine the <b>SrcBlendAlpha</b> and <b>DestBlendAlpha</b> operations.


### -field LogicOp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh404484(v=VS.85).aspx">D3D11_LOGIC_OP</a></b>

A  <a href="https://msdn.microsoft.com/en-us/library/Hh404484(v=VS.85).aspx">D3D11_LOGIC_OP</a>-typed value that specifies the logical operation to configure for the render target.


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A write mask.


## -remarks



You specify an array of <b>D3D11_RENDER_TARGET_BLEND_DESC1</b> structures in the <b>RenderTarget</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Hh404435(v=VS.85).aspx">D3D11_BLEND_DESC1</a> structure to describe the blend states for render targets; you can bind up to eight render targets to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> at one time.

For info about how blending is done, see the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.

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
<td>D3D11_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlend</td>
<td>D3D11_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOp</td>
<td>D3D11_BLEND_OP_ADD</td>
</tr>
<tr>
<td>SrcBlendAlpha</td>
<td>D3D11_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlendAlpha</td>
<td>D3D11_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOpAlpha</td>
<td>D3D11_BLEND_OP_ADD</td>
</tr>
<tr>
<td>LogicOp</td>
<td>D3D11_LOGIC_OP_NOOP</td>
</tr>
<tr>
<td>RenderTargetWriteMask</td>
<td>D3D11_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

