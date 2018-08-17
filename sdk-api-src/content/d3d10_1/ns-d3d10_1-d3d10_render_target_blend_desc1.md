---
UID: NS:d3d10_1.D3D10_RENDER_TARGET_BLEND_DESC1
title: D3D10_RENDER_TARGET_BLEND_DESC1
author: windows-sdk-content
description: Describes the blend state for a render target for a Direct3D 10.1 device
old-location: direct3d10\d3d10_render_target_blend_desc1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_render_target_blend_desc1.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 156d7844-9096-dc1b-d77b-cafba490af86, D3D10_RENDER_TARGET_BLEND_DESC1, D3D10_RENDER_TARGET_BLEND_DESC1 structure [Direct3D 10], d3d10_1/D3D10_RENDER_TARGET_BLEND_DESC1, direct3d10.d3d10_render_target_blend_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10_1.h
req.include-header: D3D10.h
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
req.typenames: D3D10_RENDER_TARGET_BLEND_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1.h
api_name:
 - D3D10_RENDER_TARGET_BLEND_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_RENDER_TARGET_BLEND_DESC1 structure


## -description


Describes the blend state for a render target for a Direct3D 10.1 device


## -struct-fields




### -field BlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable (or disable) blending.


### -field SrcBlend

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the first RGB data source and includes an optional pre-blend operation.


### -field DestBlend

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the second RGB data source and includes an optional pre-blend operation.


### -field BlendOp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204894(v=VS.85).aspx">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204894(v=VS.85).aspx">blend operation</a> defines how to combine the RGB data sources.


### -field SrcBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the first alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field DestBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the second alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field BlendOpAlpha

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204894(v=VS.85).aspx">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/en-us/library/Bb204894(v=VS.85).aspx">blend operation</a> defines how to combine the alpha data sources.


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A write mask.


## -remarks



To see how blending is done, see <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">Output-Merger Stage (Direct3D 10)</a>.

These are the default values for blend state.

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
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlend</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOp</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>SrcBlendAlpha</td>
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>DestBlendAlpha</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOpAlpha</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTargetWriteMask</td>
<td>D3D10_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

