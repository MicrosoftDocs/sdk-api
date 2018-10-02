---
UID: NS:d3d11.D3D11_DEPTH_STENCIL_DESC
title: D3D11_DEPTH_STENCIL_DESC
author: windows-sdk-content
description: Describes depth-stencil state.
old-location: direct3d11\d3d11_depth_stencil_desc.htm
tech.root: direct3d11
ms.assetid: 5e136ca8-8655-4c75-9bc0-bcf3a7af930a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 36285118-9eb2-1ef6-7c18-5d5e3cdd5535, D3D11_DEPTH_STENCIL_DESC, D3D11_DEPTH_STENCIL_DESC structure [Direct3D 11], d3d11/D3D11_DEPTH_STENCIL_DESC, direct3d11.d3d11_depth_stencil_desc
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D11_DEPTH_STENCIL_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_DEPTH_STENCIL_DESC
req.redist: 
---

# D3D11_DEPTH_STENCIL_DESC structure


## -description


Describes depth-stencil state.


## -struct-fields




### -field DepthEnable

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Enable depth testing.


### -field DepthWriteMask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476113(v=VS.85).aspx">D3D11_DEPTH_WRITE_MASK</a></b>

Identify a portion of the depth-stencil buffer that can be modified by depth data (see <a href="https://msdn.microsoft.com/en-us/library/Ff476113(v=VS.85).aspx">D3D11_DEPTH_WRITE_MASK</a>).


### -field DepthFunc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476101(v=VS.85).aspx">D3D11_COMPARISON_FUNC</a></b>

A function that compares depth data against existing depth data. The function options are listed in <a href="https://msdn.microsoft.com/en-us/library/Ff476101(v=VS.85).aspx">D3D11_COMPARISON_FUNC</a>.


### -field StencilEnable

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Enable stencil testing.


### -field StencilReadMask

Type: <b>UINT8</b>

Identify a portion of the depth-stencil buffer for reading stencil data.


### -field StencilWriteMask

Type: <b>UINT8</b>

Identify a portion of the depth-stencil buffer for writing stencil data.


### -field FrontFace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476109(v=VS.85).aspx">D3D11_DEPTH_STENCILOP_DESC</a></b>

Identify how to use the results of the depth test and the stencil test for pixels whose surface normal is facing towards the camera (see <a href="https://msdn.microsoft.com/en-us/library/Ff476109(v=VS.85).aspx">D3D11_DEPTH_STENCILOP_DESC</a>).


### -field BackFace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476109(v=VS.85).aspx">D3D11_DEPTH_STENCILOP_DESC</a></b>

Identify how to use the results of the depth test and the stencil test for pixels whose surface normal is facing away from the camera (see <a href="https://msdn.microsoft.com/en-us/library/Ff476109(v=VS.85).aspx">D3D11_DEPTH_STENCILOP_DESC</a>).


## -remarks



Pass a pointer to <b>D3D11_DEPTH_STENCIL_DESC</b> to the  <a href="https://msdn.microsoft.com/en-us/library/Ff476506(v=VS.85).aspx">ID3D11Device::CreateDepthStencilState</a> method to create the depth-stencil state object.

Depth-stencil state controls how depth-stencil testing is performed by the output-merger stage.

The following table shows the default values of depth-stencil states.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>DepthEnable</td>
<td>TRUE</td>
</tr>
<tr>
<td>DepthWriteMask</td>
<td>D3D11_DEPTH_WRITE_MASK_ALL</td>
</tr>
<tr>
<td>DepthFunc</td>
<td>D3D11_COMPARISON_LESS</td>
</tr>
<tr>
<td>StencilEnable</td>
<td>FALSE</td>
</tr>
<tr>
<td>StencilReadMask</td>
<td>D3D11_DEFAULT_STENCIL_READ_MASK</td>
</tr>
<tr>
<td>StencilWriteMask</td>
<td>D3D11_DEFAULT_STENCIL_WRITE_MASK</td>
</tr>
<tr>
<td>
FrontFace.StencilFunc

and

BackFace.StencilFunc

</td>
<td>D3D11_COMPARISON_ALWAYS</td>
</tr>
<tr>
<td>
FrontFace.StencilDepthFailOp

and

BackFace.StencilDepthFailOp

</td>
<td>D3D11_STENCIL_OP_KEEP</td>
</tr>
<tr>
<td>
FrontFace.StencilPassOp

and

BackFace.StencilPassOp

</td>
<td>D3D11_STENCIL_OP_KEEP</td>
</tr>
<tr>
<td>
FrontFace.StencilFailOp

and

BackFace.StencilFailOp

</td>
<td>D3D11_STENCIL_OP_KEEP</td>
</tr>
</table>
 

The formats that support stenciling are DXGI_FORMAT_D24_UNORM_S8_UINT and DXGI_FORMAT_D32_FLOAT_S8X24_UINT.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

