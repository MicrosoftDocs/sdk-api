---
UID: NF:d3d11.ID3D11DeviceContext.GenerateMips
title: ID3D11DeviceContext::GenerateMips (d3d11.h)
description: Generates mipmaps for the given shader resource. (ID3D11DeviceContext.GenerateMips)
helpviewer_keywords: ["79d02fdb-42ae-9bb1-5d10-7110c77d29f9","GenerateMips","GenerateMips method [Direct3D 11]","GenerateMips method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GenerateMips method","ID3D11DeviceContext.GenerateMips","ID3D11DeviceContext::GenerateMips","d3d11/ID3D11DeviceContext::GenerateMips","direct3d11.id3d11devicecontext_generatemips"]
old-location: direct3d11\id3d11devicecontext_generatemips.htm
tech.root: direct3d11
ms.assetid: 43012c58-3b1a-4956-993f-4ff3f5ec7fce
ms.date: 12/05/2018
ms.keywords: 79d02fdb-42ae-9bb1-5d10-7110c77d29f9, GenerateMips, GenerateMips method [Direct3D 11], GenerateMips method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GenerateMips method, ID3D11DeviceContext.GenerateMips, ID3D11DeviceContext::GenerateMips, d3d11/ID3D11DeviceContext::GenerateMips, direct3d11.id3d11devicecontext_generatemips
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::GenerateMips
 - d3d11/ID3D11DeviceContext::GenerateMips
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GenerateMips
---

# ID3D11DeviceContext::GenerateMips


## -description

Generates mipmaps for the given shader resource.

## -parameters

### -param pShaderResourceView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a> interface that represents the shader resource.

## -remarks

You can call <b>GenerateMips</b> on any shader-resource view to generate the lower mipmap levels for the shader resource. <b>GenerateMips</b> uses the largest mipmap level of the view to recursively generate the lower levels of the mip and stops with the smallest level that is specified by the view. If the base resource wasn't created with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a>, <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_SHADER_RESOURCE</a>, and <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_GENERATE_MIPS</a>, the call to <b>GenerateMips</b> has no effect.

<a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Feature levels</a> 9.1, 9.2, and 9.3 can't support automatic generation of mipmaps for 3D (volume) textures.

Video adapters that support <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.1 and higher support generating mipmaps if you use any of these formats:


```

DXGI_FORMAT_R8G8B8A8_UNORM
DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
DXGI_FORMAT_B5G6R5_UNORM
DXGI_FORMAT_B8G8R8A8_UNORM
DXGI_FORMAT_B8G8R8A8_UNORM_SRGB
DXGI_FORMAT_B8G8R8X8_UNORM
DXGI_FORMAT_B8G8R8X8_UNORM_SRGB

```


Video adapters that support <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.2 and higher support generating mipmaps if you use any of these formats in addition to any of the formats for feature level 9.1:


```

DXGI_FORMAT_R16G16B16A16_FLOAT
DXGI_FORMAT_R16G16B16A16_UNORM
DXGI_FORMAT_R16G16_FLOAT
DXGI_FORMAT_R16G16_UNORM
DXGI_FORMAT_R32_FLOAT

```


Video adapters that support <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.3 and higher support generating mipmaps if you use any of these formats in addition to any of the formats for feature levels 9.1 and 9.2:


```

DXGI_FORMAT_R32G32B32A32_FLOAT
DXGI_FORMAT_B4G4R4A4 (optional)

```


Video adapters that support <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10 and higher support generating mipmaps if you use any of these formats in addition to any of the formats for feature levels 9.1, 9.2, and 9.3:


```

DXGI_FORMAT_R32G32B32_FLOAT (optional)
DXGI_FORMAT_R16G16B16A16_SNORM
DXGI_FORMAT_R32G32_FLOAT
DXGI_FORMAT_R10G10B10A2_UNORM
DXGI_FORMAT_R11G11B10_FLOAT
DXGI_FORMAT_R8G8B8A8_SNORM
DXGI_FORMAT_R16G16_SNORM
DXGI_FORMAT_R8G8_UNORM
DXGI_FORMAT_R8G8_SNORM
DXGI_FORMAT_R16_FLOAT
DXGI_FORMAT_R16_UNORM
DXGI_FORMAT_R16_SNORM
DXGI_FORMAT_R8_UNORM
DXGI_FORMAT_R8_SNORM
DXGI_FORMAT_A8_UNORM
DXGI_FORMAT_B5G5R5A1_UNORM (optional)

```


For all other unsupported formats, <b>GenerateMips</b> will silently fail.

## -see-also

<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
