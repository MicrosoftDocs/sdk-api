---
UID: NS:d3d11.D3D11_DEPTH_STENCIL_VIEW_DESC
title: D3D11_DEPTH_STENCIL_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresources of a texture that are accessible from a depth-stencil view.
old-location: direct3d11\d3d11_depth_stencil_view_desc.htm
tech.root: direct3d11
ms.assetid: f073a798-edd5-4e6a-a8a7-1592721ce35d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 3b37b2e7-77a6-e3c7-bed5-e8584a152e68, D3D11_DEPTH_STENCIL_VIEW_DESC, D3D11_DEPTH_STENCIL_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_DEPTH_STENCIL_VIEW_DESC, direct3d11.d3d11_depth_stencil_view_desc
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
 - D3D11_DEPTH_STENCIL_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_DEPTH_STENCIL_VIEW_DESC
req.redist: 
---

# D3D11_DEPTH_STENCIL_VIEW_DESC structure


## -description


Specifies the subresources of a texture that are accessible from a depth-stencil view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Resource data  format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>). See remarks for allowable formats.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476115(v=VS.85).aspx">D3D11_DSV_DIMENSION</a></b>

Type of resource (see <a href="https://msdn.microsoft.com/en-us/library/Ff476115(v=VS.85).aspx">D3D11_DSV_DIMENSION</a>). Specifies how a depth-stencil resource will be accessed; the value is stored in the 
        union in this structure.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A value that describes whether the texture is read only.  Pass 0 to specify that it is not read only; otherwise, pass one of the members of 
        the <a href="https://msdn.microsoft.com/en-us/library/Ff476116(v=VS.85).aspx">D3D11_DSV_FLAG</a> enumerated type.


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476229(v=VS.85).aspx">D3D11_TEX1D_DSV</a></b>

Specifies a 1D texture subresource (see <a href="https://msdn.microsoft.com/en-us/library/Ff476229(v=VS.85).aspx">D3D11_TEX1D_DSV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476225(v=VS.85).aspx">D3D11_TEX1D_ARRAY_DSV</a></b>

Specifies an array of 1D texture subresources (see <a href="https://msdn.microsoft.com/en-us/library/Ff476225(v=VS.85).aspx">D3D11_TEX1D_ARRAY_DSV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476243(v=VS.85).aspx">D3D11_TEX2D_DSV</a></b>

Specifies a 2D texture subresource (see <a href="https://msdn.microsoft.com/en-us/library/Ff476243(v=VS.85).aspx">D3D11_TEX2D_DSV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476239(v=VS.85).aspx">D3D11_TEX2D_ARRAY_DSV</a></b>

Specifies an array of 2D texture subresources (see <a href="https://msdn.microsoft.com/en-us/library/Ff476239(v=VS.85).aspx">D3D11_TEX2D_ARRAY_DSV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476236(v=VS.85).aspx">D3D11_TEX2DMS_DSV</a></b>

Specifies a multisampled 2D texture (see <a href="https://msdn.microsoft.com/en-us/library/Ff476236(v=VS.85).aspx">D3D11_TEX2DMS_DSV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476233(v=VS.85).aspx">D3D11_TEX2DMS_ARRAY_DSV</a></b>

Specifies an array of multisampled 2D textures (see <a href="https://msdn.microsoft.com/en-us/library/Ff476233(v=VS.85).aspx">D3D11_TEX2DMS_ARRAY_DSV</a>).


## -remarks



These are valid formats for a depth-stencil view:

<ul>
<li>DXGI_FORMAT_D16_UNORM</li>
<li>DXGI_FORMAT_D24_UNORM_S8_UINT</li>
<li>DXGI_FORMAT_D32_FLOAT</li>
<li>DXGI_FORMAT_D32_FLOAT_S8X24_UINT</li>
<li>DXGI_FORMAT_UNKNOWN</li>
</ul>
A depth-stencil view cannot use a typeless format.  If the format chosen is DXGI_FORMAT_UNKNOWN, then the format of the parent resource is used.

A depth-stencil-view description is needed when calling <a href="https://msdn.microsoft.com/en-us/library/Ff476507(v=VS.85).aspx">ID3D11Device::CreateDepthStencilView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

