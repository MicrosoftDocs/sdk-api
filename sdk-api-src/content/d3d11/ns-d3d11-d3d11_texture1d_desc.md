---
UID: NS:d3d11.D3D11_TEXTURE1D_DESC
title: D3D11_TEXTURE1D_DESC (d3d11.h)
description: Describes a 1D texture. (D3D11_TEXTURE1D_DESC)
helpviewer_keywords: ["D3D11_TEXTURE1D_DESC","D3D11_TEXTURE1D_DESC structure [Direct3D 11]","c0f2647b-c461-618f-f6ef-5ea6483060e8","d3d11/D3D11_TEXTURE1D_DESC","direct3d11.d3d11_texture1d_desc"]
old-location: direct3d11\d3d11_texture1d_desc.htm
tech.root: direct3d11
ms.assetid: 8523d7b1-856e-4ec8-9286-4f1f2730a428
ms.date: 12/05/2018
ms.keywords: D3D11_TEXTURE1D_DESC, D3D11_TEXTURE1D_DESC structure [Direct3D 11], c0f2647b-c461-618f-f6ef-5ea6483060e8, d3d11/D3D11_TEXTURE1D_DESC, direct3d11.d3d11_texture1d_desc
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
targetos: Windows
req.typenames: D3D11_TEXTURE1D_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEXTURE1D_DESC
 - d3d11/D3D11_TEXTURE1D_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEXTURE1D_DESC
---

# D3D11_TEXTURE1D_DESC structure


## -description

Describes a 1D texture.

## -struct-fields

### -field Width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Texture width (in texels). The  range is from 1 to D3D11_REQ_TEXTURE1D_U_DIMENSION (16384). However, the range is actually constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of mipmap levels in the texture. See the remarks in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>. Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures in the array. The  range is from 1 to D3D11_REQ_TEXTURE1D_ARRAY_AXIS_DIMENSION (2048). However, the range is actually constrained by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.

### -field Format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

Texture format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).

### -field Usage

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a></b>

Value that identifies how the texture is to be read from and written to. The most common value is D3D11_USAGE_DEFAULT; see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a> for all possible values.

### -field BindFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a>) for binding to pipeline stages. The flags can be combined by a bitwise OR. For a 1D texture, the allowable values are: D3D11_BIND_SHADER_RESOURCE, D3D11_BIND_RENDER_TARGET and D3D11_BIND_DEPTH_STENCIL.

### -field CPUAccessFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a bitwise OR.

### -field MiscFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a bitwise OR.

## -remarks

This structure is used in a call to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture1d">ID3D11Device::CreateTexture1D</a>.

In addition to this structure, you can also use the <a href="/previous-versions/windows/desktop/legacy/jj151694(v=vs.85)">CD3D11_TEXTURE1D_DESC</a> derived structure, which is defined  in D3D11.h and behaves like an inherited class, to help create a texture description.

The texture size range is determined by the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> at which you create the device and not the Microsoft Direct3D interface version. For example, if you use Microsoft Direct3D 10 hardware at feature level 10 (<a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_10_0</a>) and call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> to create an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>, you must constrain the maximum texture size to D3D10_REQ_TEXTURE1D_U_DIMENSION (8192) when you create your 1D texture.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
