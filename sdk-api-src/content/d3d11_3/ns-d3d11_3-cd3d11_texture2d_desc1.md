---
UID: NS:d3d11_3.CD3D11_TEXTURE2D_DESC1
title: CD3D11_TEXTURE2D_DESC1 (d3d11_3.h)
description: The CD3D11_TEXTURE2D_DESC1 (d3d11_3.h) structure describes a 2D texture.
helpviewer_keywords: ["CD3D11_TEXTURE2D_DESC1","D3D11_TEXTURE2D_DESC1","D3D11_TEXTURE2D_DESC1 structure [Direct3D 11]","d3d11_3/D3D11_TEXTURE2D_DESC1","direct3d11.d3d11_texture2d_desc1"]
old-location: direct3d11\d3d11_texture2d_desc1.htm
tech.root: direct3d11
ms.assetid: DADDC12C-CF1E-48B4-B8C0-3029EC6B711B
ms.date: 08/10/2022
ms.keywords: CD3D11_TEXTURE2D_DESC1, D3D11_TEXTURE2D_DESC1, D3D11_TEXTURE2D_DESC1 structure [Direct3D 11], d3d11_3/D3D11_TEXTURE2D_DESC1, direct3d11.d3d11_texture2d_desc1
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
 - CD3D11_TEXTURE2D_DESC1
 - d3d11_3/CD3D11_TEXTURE2D_DESC1
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
 - D3D11_TEXTURE2D_DESC1
---

# CD3D11_TEXTURE2D_DESC1 structure


## -description

Describes a 2D texture.

## -struct-fields

### -field CD3D11_TEXTURE2D_DESC1

TBD

### -field ~CD3D11_TEXTURE2D_DESC1

TBD

### -field operator const D3D11_TEXTURE2D_DESC1&

TBD

### -field D3D11_TEXTURE2D_DESC1

 




#### - ArraySize

Number of textures in the texture array. The  range is from 1 to D3D11_REQ_TEXTURE2D_ARRAY_AXIS_DIMENSION (2048). For a texture cube-map, this value is a multiple of 6 (that is, 6 times the value in the <b>NumCubes</b> member of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv">D3D11_TEXCUBE_ARRAY_SRV</a>), and the  range is from 6 to 2046. The range is actually constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


#### - BindFlags

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a>) for binding to pipeline stages. The flags can be combined by a bitwise OR.


#### - CPUAccessFlags

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a bitwise OR.


#### - Format

Texture format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).


#### - Height

Texture height (in texels). The  range is from 1 to D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION (16384). For a texture cube-map, the  range is from 1 to D3D11_REQ_TEXTURECUBE_DIMENSION (16384). However, the range is actually constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


#### - MipLevels

The maximum number of mipmap levels in the texture. See the remarks in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>. Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


#### - MiscFlags

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined by using a bitwise OR. For a texture cube-map, set the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_TEXTURECUBE</a> flag. Cube-map arrays (that is, <b>ArraySize</b> &gt; 6) require feature level <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_10_1</a> or higher.


#### - SampleDesc

Structure that specifies multisampling parameters for the texture. See <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a>.


#### - TextureLayout

A <a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_texture_layout">D3D11_TEXTURE_LAYOUT</a>-typed value that identifies the layout of the texture.

The TextureLayout parameter selects both the actual layout of the texture in memory and the layout visible to the application while the texture is mapped.  These flags may not be requested without CPU access also requested.

It is illegal to set CPU access flags on default textures without also setting TextureLayout to a value other than D3D11_TEXTURE_LAYOUT_UNDEFINED.  

D3D11_TEXTURE_LAYOUT_ROW_MAJOR may only be used to create non-multisampled, textures with a single subresource (Planar YUV textures are supported).  These textures may only be used as a source and destination of copy operations, and BindFlags must be zero.


D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE may only be used to create non-multisampled, non-depth-stencil textures.  


#### - Usage

Value that identifies how the texture is to be read from and written to. The most common value is D3D11_USAGE_DEFAULT; see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a> for all possible values.


#### - Width

Texture width (in texels). The  range is from 1 to D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION (16384). For a texture cube-map, the  range is from 1 to D3D11_REQ_TEXTURECUBE_DIMENSION (16384). However, the range is actually constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.

## -remarks

This structure is used in a call to <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createtexture2d1">ID3D11Device3::CreateTexture2D1</a>.

In addition to this structure, you can also use the <b>CD3D11_TEXTURE2D_DESC1</b> derived structure, which is defined  in D3D11_3.h and behaves like an inherited class, to help create a texture description.

The device places some size restrictions (must be multiples of a minimum size) for a subsampled, block compressed, or bit-format resource.

The texture size range is determined by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the device and not the Microsoft Direct3D interface version. For example, if you use Microsoft Direct3D 10 hardware at feature level 10 (<a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_10_0</a>) and call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> to create an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>, you must constrain the maximum texture size to D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION (8192) when you create your 2D texture.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
