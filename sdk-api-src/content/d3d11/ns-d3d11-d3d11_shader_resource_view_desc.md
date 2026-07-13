---
UID: NS:d3d11.D3D11_SHADER_RESOURCE_VIEW_DESC
title: D3D11_SHADER_RESOURCE_VIEW_DESC (d3d11.h)
description: Describes a shader-resource view. (D3D11_SHADER_RESOURCE_VIEW_DESC)
helpviewer_keywords: ["13e27562-b43d-82ba-4ced-1227c27884e5","D3D11_SHADER_RESOURCE_VIEW_DESC","D3D11_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 11]","d3d11/D3D11_SHADER_RESOURCE_VIEW_DESC","direct3d11.d3d11_shader_resource_view_desc"]
old-location: direct3d11\d3d11_shader_resource_view_desc.htm
tech.root: direct3d11
ms.assetid: 7ce09172-8a01-4718-b0ef-0ae118a9be16
ms.date: 12/05/2018
ms.keywords: 13e27562-b43d-82ba-4ced-1227c27884e5, D3D11_SHADER_RESOURCE_VIEW_DESC, D3D11_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_SHADER_RESOURCE_VIEW_DESC, direct3d11.d3d11_shader_resource_view_desc
req.header: d3d11.h
req.include-header: D3D11Shader.h
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
req.typenames: D3D11_SHADER_RESOURCE_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_SHADER_RESOURCE_VIEW_DESC
 - d3d11/D3D11_SHADER_RESOURCE_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_SHADER_RESOURCE_VIEW_DESC
---

# D3D11_SHADER_RESOURCE_VIEW_DESC structure


## -description

Describes a shader-resource view.

## -struct-fields

### -field Format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> specifying the viewing format. See remarks.

### -field ViewDimension

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)">D3D11_SRV_DIMENSION</a></b>

The resource type of the view. See <a href="/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)">D3D11_SRV_DIMENSION</a>. You must set *ViewDimension* to the same resource type as that of the underlying resource. This parameter also determines which _SRV to use in the union below.

### -field Buffer

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_srv">D3D11_BUFFER_SRV</a></b>

View the resource as a buffer using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_srv">D3D11_BUFFER_SRV</a>).

### -field Texture1D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a></b>

View the resource as a 1D texture using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>).

### -field Texture1DArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_srv">D3D11_TEX1D_ARRAY_SRV</a></b>

View the resource as a 1D-texture array using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_srv">D3D11_TEX1D_ARRAY_SRV</a>).

### -field Texture2D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_srv">D3D11_TEX2D_SRV</a></b>

View the resource as a 2D-texture using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_srv">D3D11_TEX2D_SRV</a>).

### -field Texture2DArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_array_srv">D3D11_TEX2D_ARRAY_SRV</a></b>

View the resource as a 2D-texture array using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_array_srv">D3D11_TEX2D_ARRAY_SRV</a>).

### -field Texture2DMS

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_srv">D3D11_TEX2DMS_SRV</a></b>

View the resource as a 2D-multisampled texture using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_srv">D3D11_TEX2DMS_SRV</a>).

### -field Texture2DMSArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_srv">D3D11_TEX2DMS_ARRAY_SRV</a></b>

View the resource as a 2D-multisampled-texture array using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_srv">D3D11_TEX2DMS_ARRAY_SRV</a>).

### -field Texture3D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_srv">D3D11_TEX3D_SRV</a></b>

View the resource as a 3D texture using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_srv">D3D11_TEX3D_SRV</a>).

### -field TextureCube

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_srv">D3D11_TEXCUBE_SRV</a></b>

View the resource as a 3D-cube texture using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_srv">D3D11_TEXCUBE_SRV</a>).

### -field TextureCubeArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv">D3D11_TEXCUBE_ARRAY_SRV</a></b>

View the resource as a 3D-cube-texture array using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv">D3D11_TEXCUBE_ARRAY_SRV</a>).

### -field BufferEx

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_bufferex_srv">D3D11_BUFFEREX_SRV</a></b>

View the resource as a raw buffer using information from a shader-resource view (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_bufferex_srv">D3D11_BUFFEREX_SRV</a>). For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

## -remarks

A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.

When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>. To view a shader-resource-view description, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11shaderresourceview-getdesc">ID3D11ShaderResourceView::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
