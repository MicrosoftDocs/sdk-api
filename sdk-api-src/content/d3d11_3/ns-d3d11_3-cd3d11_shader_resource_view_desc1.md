---
UID: NS:d3d11_3.CD3D11_SHADER_RESOURCE_VIEW_DESC1
title: CD3D11_SHADER_RESOURCE_VIEW_DESC1 (d3d11_3.h)
description: Describes a shader-resource view.D
helpviewer_keywords: ["CD3D11_SHADER_RESOURCE_VIEW_DESC1","D3D11_SHADER_RESOURCE_VIEW_DESC1","D3D11_SHADER_RESOURCE_VIEW_DESC1 structure [Direct3D 11]","d3d11_3/D3D11_SHADER_RESOURCE_VIEW_DESC1","direct3d11.d3d11_shader_resource_view_desc1"]
old-location: direct3d11\d3d11_shader_resource_view_desc1.htm
tech.root: direct3d11
ms.assetid: 051F58C1-E3F3-4205-B834-7A14FEDFED2C
ms.date: 12/05/2018
ms.keywords: CD3D11_SHADER_RESOURCE_VIEW_DESC1, D3D11_SHADER_RESOURCE_VIEW_DESC1, D3D11_SHADER_RESOURCE_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_SHADER_RESOURCE_VIEW_DESC1, direct3d11.d3d11_shader_resource_view_desc1
req.header: d3d11_3.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_SHADER_RESOURCE_VIEW_DESC1
 - d3d11_3/CD3D11_SHADER_RESOURCE_VIEW_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_SHADER_RESOURCE_VIEW_DESC1
---

# CD3D11_SHADER_RESOURCE_VIEW_DESC1 structure


## -description

Describes a shader-resource view.

## -struct-fields

### -field CD3D11_SHADER_RESOURCE_VIEW_DESC1

TBD

### -field ~CD3D11_SHADER_RESOURCE_VIEW_DESC1

TBD

### -field operator const D3D11_SHADER_RESOURCE_VIEW_DESC1&

TBD

### -field D3D11_SHADER_RESOURCE_VIEW_DESC1

 




#### - Buffer

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_srv">D3D11_BUFFER_SRV</a> structure that views the resource as a buffer.


#### - BufferEx

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_bufferex_srv">D3D11_BUFFEREX_SRV</a> structure that views the resource as a raw buffer. For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.


#### - Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that  specifies the viewing format. See remarks.


#### - Texture1D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a> structure that views the resource as a 1D texture.


#### - Texture1DArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_srv">D3D11_TEX1D_ARRAY_SRV</a> structure that views the resource as a 1D-texture array.


#### - Texture2D

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_srv1">D3D11_TEX2D_SRV1</a> structure that views the resource as a 2D-texture.


#### - Texture2DArray

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_array_srv1">D3D11_TEX2D_ARRAY_SRV1</a> structure that views the resource as a 2D-texture array.


#### - Texture2DMS

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_srv">D3D11_TEX2DMS_SRV</a> structure that views the resource as a 2D-multisampled texture.


#### - Texture2DMSArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_srv">D3D11_TEX2DMS_ARRAY_SRV</a> structure that views the resource as a 2D-multisampled-texture array.


#### - Texture3D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_srv">D3D11_TEX3D_SRV</a> structure that views the resource as a 3D texture.


#### - TextureCube

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_srv">D3D11_TEXCUBE_SRV</a> structure that views the resource as a 3D-cube texture.


#### - TextureCubeArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv">D3D11_TEXCUBE_ARRAY_SRV</a> structure that views the resource as a 3D-cube-texture array.


#### - ViewDimension

A <a href="/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)">D3D11_SRV_DIMENSION</a>-typed value that  specifies the resource type of the view. This type is the same as the resource type of the underlying resource. This member also determines which _SRV to use in the union below.

## -remarks

A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.

When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createshaderresourceview1">ID3D11Device3::CreateShaderResourceView1</a>. To view a shader-resource-view description, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11shaderresourceview1-getdesc1">ID3D11ShaderResourceView1::GetDesc1</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
