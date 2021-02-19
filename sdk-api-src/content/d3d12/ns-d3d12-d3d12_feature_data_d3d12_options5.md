---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS5
title: D3D12_FEATURE_DATA_D3D12_OPTIONS5 (d3d12.h)
description: Indicates the level of support that the adapter provides for render passes, ray tracing, and shader-resource view tier 3 tiled resources.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS5","D3D12_FEATURE_DATA_D3D12_OPTIONS5 structure","PD3D12_FEATURE_DATA_D3D12_OPTIONS5","PD3D12_FEATURE_DATA_D3D12_OPTIONS5 structure pointer","d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS5","d3d12/PD3D12_FEATURE_DATA_D3D12_OPTIONS5","direct3d12.d3d12_feature_data_d3d12_options5"]
old-location: direct3d12\d3d12_feature_data_d3d12_options5.htm
tech.root: direct3d12
ms.assetid: 7B786C22-56C1-44A0-BE67-DE04EB367FD2
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS5, D3D12_FEATURE_DATA_D3D12_OPTIONS5 structure, PD3D12_FEATURE_DATA_D3D12_OPTIONS5, PD3D12_FEATURE_DATA_D3D12_OPTIONS5 structure pointer, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS5, d3d12/PD3D12_FEATURE_DATA_D3D12_OPTIONS5, direct3d12.d3d12_feature_data_d3d12_options5
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS5
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS5
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS5
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS5
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS5 structure


## -description

Indicates the level of support that the adapter provides for render passes, ray tracing, and shader-resource view tier 3 tiled resources.

## -struct-fields

### -field SRVOnlyTiledResourceTier3

A boolean value indicating whether the options require shader-resource view tier 3 tiled resource support. For more information, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier">D3D12_TILED_RESOURCES_TIER</a>.

### -field RenderPassesTier

The extent to which a device driver and/or the hardware efficiently supports render passes. See <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier">D3D12_RENDERPASS_TIER</a>.



#### RaytracingTier

Specifies the level of ray tracing support on the graphics device. See <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier">D3D12_RAYTRACING_TIER</a>.

### -field RaytracingTier

## -remarks

Pass <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE_D3D12_OPTIONS5</a> to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">ID3D12Device::CheckFeatureSupport</a> to retrieve a <b>D3D12_FEATURE_DATA_D3D12_OPTIONS5</b> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
