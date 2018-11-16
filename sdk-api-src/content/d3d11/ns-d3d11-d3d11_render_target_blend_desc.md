---
UID: NS:d3d11.D3D11_RENDER_TARGET_BLEND_DESC
title: D3D11_RENDER_TARGET_BLEND_DESC
author: windows-sdk-content
description: Describes the blend state for a render target.
old-location: direct3d11\d3d11_render_target_blend_desc.htm
tech.root: direct3d11
ms.assetid: 380435e9-e723-4b8b-a0bb-9ff7b4658cdc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_RENDER_TARGET_BLEND_DESC, D3D11_RENDER_TARGET_BLEND_DESC structure [Direct3D 11], b9385251-2030-9e95-a5f0-6bdef2d1d699, d3d11/D3D11_RENDER_TARGET_BLEND_DESC, direct3d11.d3d11_render_target_blend_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_RENDER_TARGET_BLEND_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_RENDER_TARGET_BLEND_DESC
req.redist: 
---

# D3D11_RENDER_TARGET_BLEND_DESC structure


## -description


Describes the blend state for a render target.


## -struct-fields




### -field BlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable (or disable) blending.


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


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A write mask.


## -remarks



You specify an array of <b>D3D11_RENDER_TARGET_BLEND_DESC</b> structures in the <b>RenderTarget</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ff476087(v=VS.85).aspx">D3D11_BLEND_DESC</a> structure to describe the blend states for render targets; you can bind up to eight render targets to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> at one time.

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
<td>RenderTargetWriteMask</td>
<td>D3D11_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

