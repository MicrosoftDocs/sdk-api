---
UID: NE:d3d12.D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
title: D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
description: Defines constants that specify a cross-API sharing support tier.
ms.date: 05/20/2019
ms.keywords: D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER
ms.topic: language-reference
f1_keywords: 
 - "d3d12/D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER"
dev_langs:
 - c++
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
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

## -enum-fields

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_0

Specifies the most basic level of cross-API sharing is supported.

### -field D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER_1

Specifies that cross-API sharing functionality of Tier 0 is supported, plus the following formats:
* DXGI_FORMAT_R16G16B16A16_TYPELESS,
* DXGI_FORMAT_R10G10B10A2_TYPELESS,
* DXGI_FORMAT_R8G8B8A8_TYPELESS,
* DXGI_FORMAT_R8G8B8X8_TYPELESS,
* DXGI_FORMAT_R16G16_TYPELESS,
* DXGI_FORMAT_R8G8_TYPELESS,
* DXGI_FORMAT_R32_TYPELESS,
* DXGI_FORMAT_R16_TYPELESS,
* DXGI_FORMAT_R8_TYPELESS

This level support is built into WDDM 2.4.

## -remarks

## -see-also
