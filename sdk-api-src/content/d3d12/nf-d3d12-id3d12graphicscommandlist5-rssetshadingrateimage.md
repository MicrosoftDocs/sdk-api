---
UID: NF:d3d12.ID3D12GraphicsCommandList5.RSSetShadingRateImage
title: ID3D12GraphicsCommandList5::RSSetShadingRateImage
description: The ID3D12GraphicsCommandList5::RSSetShadingRateImage method (d3d12.h) sets the screen-space shading-rate image for variable-rate shading (VRS).
tech.root: direct3d12
ms.date: 08/10/2022
ms.keywords: ID3D12GraphicsCommandList5::RSSetShadingRateImage
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
 - ID3D12GraphicsCommandList5::RSSetShadingRateImage
 - d3d12/ID3D12GraphicsCommandList5::RSSetShadingRateImage
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12GraphicsCommandList5::RSSetShadingRateImage
---

## -description

Sets the screen-space shading-rate image for variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs).
This method requires Tier2 [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs) support. See [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) and [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier).

## -parameters

### -param shadingRateImage

Type: **[ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

An optional pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing a screen-space shading-rate image.
If **NULL**, the effect is the same as having a shading-rate image where all values are a shading rate of 1x1.

This texture must have the [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state applied.

The tile-size of the shading-rate image can be determined via [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6).
The size of the shading-rate image should therefore be
```
ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize)
```

The shading-rate image must be a 2D texture with a single mip, and format [**DXGI_FORMAT_R8_UINT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Each texel must be a value corresponding to [**D3D12_SHADING_RATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate). It must have layout [**D3D12_TEXTURE_LAYOUT_UNKNOWN**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout) and can't be a depth-stencil, render-target, simultaneous-access, or cross-adapter resource.

As (0, 0) is the top left in DirectX, a too-small or large shading-rate image results in the bottom or right having no shading-rate image area, or the image extending in these directions. When there is excess, it is ignored (but legal), and when the image is too small, all out-of-bounds areas in the bottom and right will have the default shading rate of 1x1 from the image (however, this does not mean that is the final shading rate. The combiners will still be applied to this 1x1 default value).

## -remarks

For the screen-space shading-rate image to take affect, [**ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) must have been called to set the combiners for shading. Else, with the default combiners (both [**D3D12_SHADING_RATE_COMBINER_PASSTHROUGH**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner)), the screen-space shading-rate image is ignored in determining shading granularity.

The second combiner passed to  [**ID3D12GraphicsCommandList5::RSSetShadingRate**] is the one which applies to the shading-rate image, which occurs after the global shading rate and the per-primitive shading rate have been combined.

The algorithm for final shading-rate is determined by

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

## -see-also

[Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)

