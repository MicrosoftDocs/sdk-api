---
UID: NE:d3d12.D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
title: D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
description: Defines constants that specify a cross-API sharing support tier.
tech.root: direct3d12
helpviewer_keywords: ["D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER"]
ms.date: 05/20/2019
ms.keywords: D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
 - d3d12/D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
---

## -description

Defines constants that specify a cross-API sharing support tier.

The resource data formats mentioned are members of the [DXGI_FORMAT enumeration](../dxgiformat/ne-dxgiformat-dxgi_format.md).

## -enum-fields

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_0:0

Specifies that the most basic level of cross-API sharing is supported, including the following resource data formats.

* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_B8G8R8X8_UNORM_SRGB
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R16G16B16A16_FLOAT

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_1

Specifies that cross-API sharing functionality of Tier 0 is supported, plus the following formats.

* DXGI_FORMAT_R16G16B16A16_TYPELESS
* DXGI_FORMAT_R10G10B10A2_TYPELESS
* DXGI_FORMAT_R8G8B8A8_TYPELESS
* DXGI_FORMAT_R8G8B8X8_TYPELESS
* DXGI_FORMAT_R16G16_TYPELESS
* DXGI_FORMAT_R8G8_TYPELESS
* DXGI_FORMAT_R32_TYPELESS
* DXGI_FORMAT_R16_TYPELESS
* DXGI_FORMAT_R8_TYPELESS

This level support is built into WDDM 2.4.

Also see [Extended support for shared Texture2D resources](/windows/win32/direct3d11/direct3d-11-1-features#extended-support-for-shared-texture2d-resources).

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_2

Specifies that cross-API sharing functionality of Tier 1 is supported, plus the following formats.

* DXGI_FORMAT_NV12 (also see [Extended NV12 texture support](/windows/win32/direct3d11/direct3d-11-4-features#extended-nv12-texture-support))

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_3

Specifies that cross-API sharing functionality of Tier 2 is supported, plus the following formats.

* DXGI_FORMAT_R11G11B10_FLOAT

## -remarks

## -see-also
