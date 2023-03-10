---
UID: NS:d3d12.D3D12_DEPTH_STENCIL_VIEW_DESC
title: D3D12_DEPTH_STENCIL_VIEW_DESC (d3d12.h)
description: Describes the subresources of a texture that are accessible from a depth-stencil view.
helpviewer_keywords: ["D3D12_DEPTH_STENCIL_VIEW_DESC","D3D12_DEPTH_STENCIL_VIEW_DESC structure","d3d12/D3D12_DEPTH_STENCIL_VIEW_DESC","direct3d12.d3d12_depth_stencil_view_desc"]
old-location: direct3d12\d3d12_depth_stencil_view_desc.htm
tech.root: direct3d12
ms.assetid: 53161933-5B3B-4B38-AC70-46A4164AE072
ms.date: 12/05/2018
ms.keywords: D3D12_DEPTH_STENCIL_VIEW_DESC, D3D12_DEPTH_STENCIL_VIEW_DESC structure, d3d12/D3D12_DEPTH_STENCIL_VIEW_DESC, direct3d12.d3d12_depth_stencil_view_desc
req.header: d3d12.h
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
targetos: Windows
req.typenames: D3D12_DEPTH_STENCIL_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEPTH_STENCIL_VIEW_DESC
 - d3d12/D3D12_DEPTH_STENCIL_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DEPTH_STENCIL_VIEW_DESC
---

# D3D12_DEPTH_STENCIL_VIEW_DESC structure


## -description

Describes the subresources of a texture that are accessible from a depth-stencil view.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the viewing format.  For allowable formats, see Remarks.

### -field ViewDimension

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension">D3D12_DSV_DIMENSION</a>-typed value that specifies how the depth-stencil resource will be accessed. This member also determines which _DSV to use in the following union.

### -field Flags

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags">D3D12_DSV_FLAGS</a> enumeration constants that are combined by using a bitwise OR operation. 
            The resulting value specifies whether the texture is read only.  
            Pass 0 to specify that it isn't read only; otherwise, pass one or more of the members of the <b>D3D12_DSV_FLAGS</b> enumerated type.

### -field Texture1D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv">D3D12_TEX1D_DSV</a> structure that specifies a 1D texture subresource.

### -field Texture1DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv">D3D12_TEX1D_ARRAY_DSV</a> structure that specifies an array of 1D texture subresources.

### -field Texture2D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv">D3D12_TEX2D_DSV</a> structure that specifies a 2D texture subresource.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv">D3D12_TEX2D_ARRAY_DSV</a> structure that specifies an array of 2D texture subresources.

### -field Texture2DMS

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv">D3D12_TEX2DMS_DSV</a> structure that specifies a multisampled 2D texture.

### -field Texture2DMSArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv">D3D12_TEX2DMS_ARRAY_DSV</a> structure that specifies an array of multisampled 2D textures.

## -remarks

These are valid formats for a depth-stencil view:
        

<ul>
<li>DXGI_FORMAT_D16_UNORM</li>
<li>DXGI_FORMAT_D24_UNORM_S8_UINT</li>
<li>DXGI_FORMAT_D32_FLOAT</li>
<li>DXGI_FORMAT_D32_FLOAT_S8X24_UINT</li>
<li>DXGI_FORMAT_UNKNOWN</li>
</ul>
A depth-stencil view can't use a typeless format.  If the format chosen is DXGI_FORMAT_UNKNOWN, the format of the parent resource is used.
        

Pass a depth-stencil-view description into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview">ID3D12Device::CreateDepthStencilView</a> to create a depth-stencil view.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>