---
UID: NS:d3d10.CD3D10_TEXTURE3D_DESC
title: CD3D10_TEXTURE3D_DESC (d3d10.h)
description: The CD3D10_TEXTURE3D_DESC (d3d10.h) structure describes a 3D texture.
helpviewer_keywords: ["CD3D10_TEXTURE3D_DESC","D3D10_TEXTURE3D_DESC","D3D10_TEXTURE3D_DESC structure [Direct3D 10]","abbd74e0-643f-c06c-689d-08361a07731d","d3d10/D3D10_TEXTURE3D_DESC","direct3d10.d3d10_texture3d_desc"]
old-location: direct3d10\d3d10_texture3d_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texture3d_desc.htm
ms.date: 08/10/2022
ms.keywords: CD3D10_TEXTURE3D_DESC, D3D10_TEXTURE3D_DESC, D3D10_TEXTURE3D_DESC structure [Direct3D 10], abbd74e0-643f-c06c-689d-08361a07731d, d3d10/D3D10_TEXTURE3D_DESC, direct3d10.d3d10_texture3d_desc
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D10_TEXTURE3D_DESC
 - d3d10/CD3D10_TEXTURE3D_DESC
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
 - D3D10_TEXTURE3D_DESC
---

## -description

Describes a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">3D texture</a>.

## -struct-fields

## -remarks

`format`
Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>
Texture format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).

`width`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Texture width (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). For more information about restrictions, see Remarks.

`height`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Texture height (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). For more information about restrictions, see Remarks.

`depth`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Texture depth (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048).

`mipLevels`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Number of subtextures (also called mipmap levels). Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.

`bindFlags`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_FLAG</a>) for binding to <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a> stages. The flags can be combined by a logical OR.

`usage`
Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a></b>
Value that identifies how the texture is to be read from and written to. The most common value is D3D10_USAGE-DEFAULT; see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a> for all possible values.

`cpuAccessFlags`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.

`miscFlags`
Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>
Flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a logical OR.

This structure is used in a call to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture3d">ID3D10Device::CreateTexture3D</a>. A helpful derived structure CD3D10_TEXTURE3D_DESC is declared in D3D10.h, to help create a texture description.

The device restricts the size of subsampled, block compressed (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Block Compression (Direct3D 10)</a>), and bit format resources to be multiples of sizes specific to each format.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource structures</a>
