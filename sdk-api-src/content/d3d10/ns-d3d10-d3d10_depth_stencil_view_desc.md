---
UID: NS:d3d10.D3D10_DEPTH_STENCIL_VIEW_DESC
title: D3D10_DEPTH_STENCIL_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresource(s) from a texture that are accessible using a depth-stencil view.
old-location: direct3d10\d3d10_depth_stencil_view_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencil_view_desc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_DEPTH_STENCIL_VIEW_DESC, D3D10_DEPTH_STENCIL_VIEW_DESC structure [Direct3D 10], bc861c79-f54d-480a-d677-9bbbd949112b, d3d10/D3D10_DEPTH_STENCIL_VIEW_DESC, direct3d10.d3d10_depth_stencil_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
req.typenames: D3D10_DEPTH_STENCIL_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_DEPTH_STENCIL_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_DEPTH_STENCIL_VIEW_DESC structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from a texture that are accessible using a depth-stencil view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Resource data  format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>). See remarks for allowable formats.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205043(v=VS.85).aspx">D3D10_DSV_DIMENSION</a></b>

Type of resource (see <a href="https://msdn.microsoft.com/en-us/library/Bb205043(v=VS.85).aspx">D3D10_DSV_DIMENSION</a>). Specifies how a depth-stencil resource will be accessed; the value is stored in the union in this structure.


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172461(v=VS.85).aspx">D3D10_TEX1D_DSV</a></b>

Specifies a 1D texture subresource (see <a href="https://msdn.microsoft.com/en-us/library/Bb172461(v=VS.85).aspx">D3D10_TEX1D_DSV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172458(v=VS.85).aspx">D3D10_TEX1D_ARRAY_DSV</a></b>

Specifies an array of 1D texture subresources (see <a href="https://msdn.microsoft.com/en-us/library/Bb172458(v=VS.85).aspx">D3D10_TEX1D_ARRAY_DSV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172473(v=VS.85).aspx">D3D10_TEX2D_DSV</a></b>

Specifies a 2D texture subresource (see <a href="https://msdn.microsoft.com/en-us/library/Bb172473(v=VS.85).aspx">D3D10_TEX2D_DSV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172470(v=VS.85).aspx">D3D10_TEX2D_ARRAY_DSV</a></b>

Specifies an array of 2D texture subresources (see <a href="https://msdn.microsoft.com/en-us/library/Bb172470(v=VS.85).aspx">D3D10_TEX2D_ARRAY_DSV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172467(v=VS.85).aspx">D3D10_TEX2DMS_DSV</a></b>

Specifies a multisampled 2D texture contains a single subresource (see <a href="https://msdn.microsoft.com/en-us/library/Bb172467(v=VS.85).aspx">D3D10_TEX2DMS_DSV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172464(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_DSV</a></b>

Specifies a multisampled 2D texture contains a single subresource per texture (see <a href="https://msdn.microsoft.com/en-us/library/Bb172464(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_DSV</a>).


## -remarks



These are valid formats for a depth-stencil view:

<ul>
<li>DXGI_FORMAT_D16_UNORM</li>
<li>DXGI_FORMAT_D24_UNORM_S8_UINT</li>
<li>DXGI_FORMAT_D32_FLOAT</li>
<li>DXGI_FORMAT_D32_FLOAT_S8X24_UINT</li>
<li>DXGI_FORMAT_UNKNOWN</li>
</ul>
A depth-stencil view cannot use a <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">typeless format</a>.  If the format chosen is DXGI_FORMAT_UNKNOWN, then the format of the parent resource is used.

A depth-stencil-view description is needed when calling <a href="https://msdn.microsoft.com/en-us/library/Bb173547(v=VS.85).aspx">ID3D10Device::CreateDepthStencilView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

