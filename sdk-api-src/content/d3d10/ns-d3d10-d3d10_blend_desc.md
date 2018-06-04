---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D10_BLEND_DESC structure


## -description


Describes the blend state.


## -struct-fields




### -field AlphaToCoverageEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines whether or not to use <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">alpha-to-coverage</a> as a multisampling technique when setting a pixel to a rendertarget.


### -field BlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable (or disable) blending. There are eight elements in this array; these correspond to the eight rendertargets that can be set to output-merger stage at one time.


### -field SrcBlend

Type: <b><a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> specifies the first RGB data source and includes an optional pre-blend operation.


### -field DestBlend

Type: <b><a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> specifies the second RGB data source and includes an optional pre-blend operation.


### -field BlendOp

Type: <b><a href="https://msdn.microsoft.com/2d23109a-4d0e-4001-a693-185a942900c0">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/2d23109a-4d0e-4001-a693-185a942900c0">blend operation</a> defines how to combine the RGB data sources.


### -field SrcBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> specifies the first alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field DestBlendAlpha

Type: <b><a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">D3D10_BLEND</a></b>

This <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> specifies the second alpha data source and includes an optional pre-blend operation. Blend options that end in _COLOR are not allowed.


### -field BlendOpAlpha

Type: <b><a href="https://msdn.microsoft.com/2d23109a-4d0e-4001-a693-185a942900c0">D3D10_BLEND_OP</a></b>

This <a href="https://msdn.microsoft.com/2d23109a-4d0e-4001-a693-185a942900c0">blend operation</a> defines how to combine the alpha data sources.


### -field RenderTargetWriteMask

Type: <b>UINT8</b>

A per-pixel write mask that allows control over which components can be written (see <a href="https://msdn.microsoft.com/2d1b17ee-1631-49e3-a254-9586e548d568">D3D10_COLOR_WRITE_ENABLE</a>).


## -remarks



To see how blending is done, see <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">Output-Merger Stage (Direct3D 10)</a>.

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




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

