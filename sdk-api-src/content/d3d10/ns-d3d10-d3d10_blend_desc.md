---
UID: NS:d3d10.D3D10_BLEND_DESC
title: D3D10_BLEND_DESC
author: windows-sdk-content
description: Describes the blend state.
old-location: direct3d10\d3d10_blend_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend_desc.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 721f9aa7-5588-d838-c466-ccde084bdae9, D3D10_BLEND_DESC, D3D10_BLEND_DESC structure [Direct3D 10], d3d10/D3D10_BLEND_DESC, direct3d10.d3d10_blend_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
tech.root: 
req.typenames: D3D10_BLEND_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BLEND_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_BLEND_DESC structure


## -description


Describes the blend state.


## -struct-fields




### -field AlphaToCoverageEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines whether or not to use <a href="https://msdn.microsoft.com/library/Bb205072(v=VS.85).aspx">alpha-to-coverage</a> as a multisampling technique when setting a pixel to a rendertarget.


### -field BlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable (or disable) blending. There are eight elements in this array; these correspond to the eight rendertargets that can be set to output-merger stage at one time.


### -field SrcBlend

Type: <b><a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the first RGB data source and includes an optional pre-blend operation.


### -field DestBlend

Type: <b><a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the second RGB data source and includes an optional pre-blend operation.


### -field BlendOp

Type: <b><a href="https://msdn.microsoft.com/library/Bb204894(v=VS.85).aspx">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204894(v=VS.85).aspx">blend operation</a> defines how to combine the RGB data sources.


### -field SrcBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the first alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field DestBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204892(v=VS.85).aspx">blend option</a> specifies the second alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field BlendOpAlpha

Type: <b><a href="https://msdn.microsoft.com/library/Bb204894(v=VS.85).aspx">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/library/Bb204894(v=VS.85).aspx">blend operation</a> defines how to combine the alpha data sources.


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A per-pixel write mask that allows control over which components can be written (see <a href="https://msdn.microsoft.com/library/Bb204901(v=VS.85).aspx">D3D10_COLOR_WRITE_ENABLE</a>).


## -remarks



To see how blending is done, see <a href="https://msdn.microsoft.com/library/Bb205120(v=VS.85).aspx">Output-Merger Stage (Direct3D 10)</a>.

These are the default values for blend state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>AlphaToCoverageEnable</td>
<td>FALSE</td>
</tr>
<tr>
<td>BlendEnable[8]</td>
<td>FALSE (for all 8)</td>
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
<td>RenderTargetWriteMask[8]</td>
<td>D3D10_COLOR_WRITE_ENABLE_ALL (for all 8)</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

