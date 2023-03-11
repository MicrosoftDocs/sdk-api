---
UID: NF:d3d10.ID3D10Device.GenerateMips
title: ID3D10Device::GenerateMips (d3d10.h)
description: Generates mipmaps for the given shader resource. (ID3D10Device.GenerateMips)
helpviewer_keywords: ["46ad9ad3-37a7-33c9-7829-0dbf6d4b348a","GenerateMips","GenerateMips method [Direct3D 10]","GenerateMips method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GenerateMips method","ID3D10Device.GenerateMips","ID3D10Device::GenerateMips","d3d10/ID3D10Device::GenerateMips","direct3d10.id3d10device_generatemips"]
old-location: direct3d10\id3d10device_generatemips.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_generatemips.htm
ms.date: 12/05/2018
ms.keywords: 46ad9ad3-37a7-33c9-7829-0dbf6d4b348a, GenerateMips, GenerateMips method [Direct3D 10], GenerateMips method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GenerateMips method, ID3D10Device.GenerateMips, ID3D10Device::GenerateMips, d3d10/ID3D10Device::GenerateMips, direct3d10.id3d10device_generatemips
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GenerateMips
 - d3d10/ID3D10Device::GenerateMips
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GenerateMips
---

# ID3D10Device::GenerateMips


## -description

Generates mipmaps for the given shader resource.

## -parameters

### -param pShaderResourceView [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>. The mipmaps will be generated for this shader resource.

## -remarks

GenerateMips may be called on any ID3D10ShaderResourceView in order to generate the lower mipmap levels. GenerateMips uses the largest mipmap level of the view to recursively generate the lower levels of the mip, stopping with the smallest level specified by the view. If the base resource was not created with <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_RENDER_TARGET</a> and <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_GENERATE_MIPS</a>, this call has no effect.

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


For all other unsupported formats, this method will silently fail.

## -see-also

<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
