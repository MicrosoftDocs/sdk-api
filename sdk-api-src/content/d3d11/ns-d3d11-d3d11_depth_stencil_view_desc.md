---
UID: NS:d3d11.D3D11_DEPTH_STENCIL_VIEW_DESC
title: D3D11_DEPTH_STENCIL_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresources of a texture that are accessible from a depth-stencil view.
old-location: direct3d11\d3d11_depth_stencil_view_desc.htm
old-project: direct3d11
ms.assetid: f073a798-edd5-4e6a-a8a7-1592721ce35d
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 3b37b2e7-77a6-e3c7-bed5-e8584a152e68, D3D11_DEPTH_STENCIL_VIEW_DESC, D3D11_DEPTH_STENCIL_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_DEPTH_STENCIL_VIEW_DESC, direct3d11.d3d11_depth_stencil_view_desc
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
tech.root: 
req.typenames: D3D11_DEPTH_STENCIL_VIEW_DESC
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
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_DEPTH_STENCIL_VIEW_DESC structure


## -description


Specifies the subresources of a texture that are accessible from a depth-stencil view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Resource data  format (see <a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>). See remarks for allowable formats.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/3037e940-6915-4b1d-b0ae-cd440033ac38">D3D11_DSV_DIMENSION</a></b>

Type of resource (see <a href="https://msdn.microsoft.com/3037e940-6915-4b1d-b0ae-cd440033ac38">D3D11_DSV_DIMENSION</a>). Specifies how a depth-stencil resource will be accessed; the value is stored in the 
        union in this structure.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that describes whether the texture is read only.  Pass 0 to specify that it is not read only; otherwise, pass one of the members of 
        the <a href="https://msdn.microsoft.com/8894ec55-9d56-4d41-a5d6-72ce064e3351">D3D11_DSV_FLAG</a> enumerated type.


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/dfdbad36-3cfc-4e24-9864-ffe1405030b2">D3D11_TEX1D_DSV</a></b>

Specifies a 1D texture subresource (see <a href="https://msdn.microsoft.com/dfdbad36-3cfc-4e24-9864-ffe1405030b2">D3D11_TEX1D_DSV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/9e4233cc-680a-486e-b91a-732d055937d1">D3D11_TEX1D_ARRAY_DSV</a></b>

Specifies an array of 1D texture subresources (see <a href="https://msdn.microsoft.com/9e4233cc-680a-486e-b91a-732d055937d1">D3D11_TEX1D_ARRAY_DSV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/f3f7aeca-e6c1-445c-97f4-1968b726dad7">D3D11_TEX2D_DSV</a></b>

Specifies a 2D texture subresource (see <a href="https://msdn.microsoft.com/f3f7aeca-e6c1-445c-97f4-1968b726dad7">D3D11_TEX2D_DSV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/0cf77ebd-a83c-4021-866d-664913549d80">D3D11_TEX2D_ARRAY_DSV</a></b>

Specifies an array of 2D texture subresources (see <a href="https://msdn.microsoft.com/0cf77ebd-a83c-4021-866d-664913549d80">D3D11_TEX2D_ARRAY_DSV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/1723044b-1942-4373-8040-0c47b680ea95">D3D11_TEX2DMS_DSV</a></b>

Specifies a multisampled 2D texture (see <a href="https://msdn.microsoft.com/1723044b-1942-4373-8040-0c47b680ea95">D3D11_TEX2DMS_DSV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/e01f8473-a69d-4e69-a8e3-3916fd5e7102">D3D11_TEX2DMS_ARRAY_DSV</a></b>

Specifies an array of multisampled 2D textures (see <a href="https://msdn.microsoft.com/e01f8473-a69d-4e69-a8e3-3916fd5e7102">D3D11_TEX2DMS_ARRAY_DSV</a>).


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

A depth-stencil-view description is needed when calling <a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">ID3D11Device::CreateDepthStencilView</a>.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

