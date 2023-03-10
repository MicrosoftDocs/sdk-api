---
UID: NS:d3d10.D3D10_DEPTH_STENCIL_VIEW_DESC
title: D3D10_DEPTH_STENCIL_VIEW_DESC (d3d10.h)
description: Specifies the subresource(s) from a texture that are accessible using a depth-stencil view.
helpviewer_keywords: ["D3D10_DEPTH_STENCIL_VIEW_DESC","D3D10_DEPTH_STENCIL_VIEW_DESC structure [Direct3D 10]","bc861c79-f54d-480a-d677-9bbbd949112b","d3d10/D3D10_DEPTH_STENCIL_VIEW_DESC","direct3d10.d3d10_depth_stencil_view_desc"]
old-location: direct3d10\d3d10_depth_stencil_view_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencil_view_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_DEPTH_STENCIL_VIEW_DESC, D3D10_DEPTH_STENCIL_VIEW_DESC structure [Direct3D 10], bc861c79-f54d-480a-d677-9bbbd949112b, d3d10/D3D10_DEPTH_STENCIL_VIEW_DESC, direct3d10.d3d10_depth_stencil_view_desc
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
targetos: Windows
req.typenames: D3D10_DEPTH_STENCIL_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_DEPTH_STENCIL_VIEW_DESC
 - d3d10/D3D10_DEPTH_STENCIL_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_DEPTH_STENCIL_VIEW_DESC
---

# D3D10_DEPTH_STENCIL_VIEW_DESC structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource(s)</a> from a texture that are accessible using a depth-stencil view.

## -struct-fields

### -field Format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

Resource data  format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>). See remarks for allowable formats.

### -field ViewDimension

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_dsv_dimension">D3D10_DSV_DIMENSION</a></b>

Type of resource (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_dsv_dimension">D3D10_DSV_DIMENSION</a>). Specifies how a depth-stencil resource will be accessed; the value is stored in the union in this structure.

### -field Texture1D

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex1d_dsv">D3D10_TEX1D_DSV</a></b>

Specifies a 1D texture subresource (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex1d_dsv">D3D10_TEX1D_DSV</a>).

### -field Texture1DArray

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex1d_array_dsv">D3D10_TEX1D_ARRAY_DSV</a></b>

Specifies an array of 1D texture subresources (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex1d_array_dsv">D3D10_TEX1D_ARRAY_DSV</a>).

### -field Texture2D

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2d_dsv">D3D10_TEX2D_DSV</a></b>

Specifies a 2D texture subresource (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2d_dsv">D3D10_TEX2D_DSV</a>).

### -field Texture2DArray

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2d_array_dsv">D3D10_TEX2D_ARRAY_DSV</a></b>

Specifies an array of 2D texture subresources (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2d_array_dsv">D3D10_TEX2D_ARRAY_DSV</a>).

### -field Texture2DMS

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2dms_dsv">D3D10_TEX2DMS_DSV</a></b>

Specifies a multisampled 2D texture contains a single subresource (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2dms_dsv">D3D10_TEX2DMS_DSV</a>).

### -field Texture2DMSArray

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2dms_array_dsv">D3D10_TEX2DMS_ARRAY_DSV</a></b>

Specifies a multisampled 2D texture contains a single subresource per texture (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2dms_array_dsv">D3D10_TEX2DMS_ARRAY_DSV</a>).

## -remarks

These are valid formats for a depth-stencil view:

<ul>
<li>DXGI_FORMAT_D16_UNORM</li>
<li>DXGI_FORMAT_D24_UNORM_S8_UINT</li>
<li>DXGI_FORMAT_D32_FLOAT</li>
<li>DXGI_FORMAT_D32_FLOAT_S8X24_UINT</li>
<li>DXGI_FORMAT_UNKNOWN</li>
</ul>
A depth-stencil view cannot use a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">typeless format</a>.  If the format chosen is DXGI_FORMAT_UNKNOWN, then the format of the parent resource is used.

A depth-stencil-view description is needed when calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>