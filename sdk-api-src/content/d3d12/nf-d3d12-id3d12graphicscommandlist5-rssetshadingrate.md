---
UID: NF:d3d12.ID3D12GraphicsCommandList5.RSSetShadingRate
title: ID3D12GraphicsCommandList5::RSSetShadingRate
description: The ID3D12GraphicsCommandList5::RSSetShadingRate method (d3d12.h) sets the base shading rate, and combiners, for variable-rate shading (VRS). 
tech.root: direct3d12
ms.date: 08/10/2022
ms.keywords: ID3D12GraphicsCommandList5::RSSetShadingRate
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D12GraphicsCommandList5::RSSetShadingRate
 - d3d12/ID3D12GraphicsCommandList5::RSSetShadingRate
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12GraphicsCommandList5::RSSetShadingRate
---

## -description

Sets the base shading rate, and combiners, for variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).

## -parameters

### -param baseShadingRate

Type: [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)

A constant from the [D3D12_SHADING_RATE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) enumeration describing the base shading rate to set.

### -param combiners

Type: **const [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner)\***

An optional pointer to a constant array of [**D3D12_SHADING_RATE_COMBINER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) containing the shading rate combiners to set. The count of [**D3D12_SHADING_RATE_COMBINER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) elements in the array must be equal to the constant [**D3D12_RS_SET_SHADING_RATE_COMBINER_COUNT**](/windows/win32/direct3d12/constants), which is equal to **2**.

Because per-primitive and screen-space image-based VRS isn't supported on Tier1 [Variable-rate shading (VRS)](/windows/win32/direct3d12/vrs), for these values to be meaningful, the adapter requires Tier2 VRS support. See [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) and [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier).

A **NULL** pointer is equivalent to the default shading combiners, which are both [**D3D12_SHADING_RATE_COMBINER_PASSTHROUGH**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner).

The algorithm for final shading-rate is determined by the following.

```cpp
postRasterizerRate = ApplyCombiner(Combiners[0], CommandListShadingRate, Primitive->PrimitiveSpecifiedShadingRate);
finalRate = ApplyCombiner(Combiners[1], postRasterizerRate, ScreenSpaceImage[xy]);
```

where `ApplyCombiner` is

```cpp
UINT ApplyCombiner(D3D12_SHADING_RATE_COMBINER combiner, UINT a, UINT b)
{
    MaxShadingRate = options6.AdditionalShadingRatesSupported ? 4 : 2;
    switch (combiner)
    {
        case D3D12_SHADING_RATE_COMBINER_PASSTHROUGH: // default
            return a;
        case D3D12_SHADING_RATE_COMBINER_OVERRIDE:
            return b;
        case D3D12_SHADING_RATE_COMBINER_MAX:
            return max(a, b);
        case D3D12_SHADING_RATE_COMBINER_MIN:
            return min(a, b);
        case D3D12_SHADING_RATE_COMBINER_SUM:
            return min(MaxShadingRate, a + b);
        case default:
            return a;
    }
}
```

## -remarks

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)

