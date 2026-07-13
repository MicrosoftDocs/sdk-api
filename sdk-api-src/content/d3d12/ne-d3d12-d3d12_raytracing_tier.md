---
UID: NE:d3d12.D3D12_RAYTRACING_TIER
title: D3D12_RAYTRACING_TIER (d3d12.h)
description: Specifies the level of ray tracing support on the graphics device.
helpviewer_keywords: ["D3D12_RAYTRACING_TIER","D3D12_RAYTRACING_TIER enumeration","D3D12_RAYTRACING_TIER_1_0","D3D12_RAYTRACING_TIER_NOT_SUPPORTED","d3d12/D3D12_RAYTRACING_TIER","d3d12/D3D12_RAYTRACING_TIER_1_0","d3d12/D3D12_RAYTRACING_TIER_NOT_SUPPORTED","direct3d12.d3d12_raytracing_tier"]
old-location: direct3d12\d3d12_raytracing_tier.htm
tech.root: direct3d12
ms.assetid: 1C97DD15-5BAD-4BDC-AE43-4B6A1350B6A0
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_TIER, D3D12_RAYTRACING_TIER enumeration, D3D12_RAYTRACING_TIER_1_0, D3D12_RAYTRACING_TIER_NOT_SUPPORTED, d3d12/D3D12_RAYTRACING_TIER, d3d12/D3D12_RAYTRACING_TIER_1_0, d3d12/D3D12_RAYTRACING_TIER_NOT_SUPPORTED, direct3d12.d3d12_raytracing_tier
req.header: d3d12.h
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
req.typenames: D3D12_RAYTRACING_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_TIER
 - d3d12/D3D12_RAYTRACING_TIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RAYTRACING_TIER
---

# D3D12_RAYTRACING_TIER enumeration


## -description

Specifies the level of ray tracing support on the graphics device.

## -enum-fields

### -field D3D12_RAYTRACING_TIER_NOT_SUPPORTED:0

No support for ray tracing on the device.  Attempts to create any ray tracing-related object will fail, and using ray tracing-related APIs on command lists results in undefined behavior.

### -field D3D12_RAYTRACING_TIER_1_0:10

The device supports tier 1 ray tracing functionality. In the current release, this tier represents all available ray tracing features.

## -remarks

To determine the supported ray tracing tier for a graphics device, pass <a href="../d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5.md">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a> struct.
