---
UID: NS:d3d10.D3D10_BLEND_DESC
title: D3D10_BLEND_DESC (d3d10.h)
author: windows-sdk-content
description: Describes the blend state.
old-location: direct3d10\d3d10_blend_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend_desc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 721f9aa7-5588-d838-c466-ccde084bdae9, D3D10_BLEND_DESC, D3D10_BLEND_DESC structure [Direct3D 10], d3d10/D3D10_BLEND_DESC, direct3d10.d3d10_blend_desc
ms.topic: struct
f1_keywords: 
 - "d3d10/D3D10_BLEND_DESC"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D10_BLEND_DESC
req.redist: 
ms.custom: 19H1
---

# D3D10_BLEND_DESC structure


## -description


Describes the blend state.


## -struct-fields




### -field AlphaToCoverageEnable

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Determines whether or not to use <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">alpha-to-coverage</a> as a multisampling technique when setting a pixel to a rendertarget.


### -field BlendEnable

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Enable (or disable) blending. There are eight elements in this array; these correspond to the eight rendertargets that can be set to output-merger stage at one time.


### -field SrcBlend

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">D3D10_BLEND</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">blend option</a> specifies the first RGB data source and includes an optional pre-blend operation.


### -field DestBlend

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">D3D10_BLEND</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">blend option</a> specifies the second RGB data source and includes an optional pre-blend operation.


### -field BlendOp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend_op">D3D10_BLEND_OP</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend_op">blend operation</a> defines how to combine the RGB data sources.


### -field SrcBlendAlpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">D3D10_BLEND</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">blend option</a> specifies the first alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field DestBlendAlpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">D3D10_BLEND</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">blend option</a> specifies the second alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field BlendOpAlpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend_op">D3D10_BLEND_OP</a></b>

This <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend_op">blend operation</a> defines how to combine the alpha data sources.


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A per-pixel write mask that allows control over which components can be written (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_color_write_enable">D3D10_COLOR_WRITE_ENABLE</a>).


## -remarks



To see how blending is done, see <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">Output-Merger Stage (Direct3D 10)</a>.

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




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
 

 

