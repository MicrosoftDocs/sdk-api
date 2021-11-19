---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS6
title: D3D12_FEATURE_DATA_D3D12_OPTIONS6
description: Indicates the level of support that the adapter provides for variable-rate shading (VRS), and indicates whether or not background processing is supported.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS6"]
tech.root: direct3d12
ms.date: 05/20/2019
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS6
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS6
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS6
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS6
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS6
---

## -description

Indicates the level of support that the adapter provides for variable-rate shading (VRS), and indicates whether or not background processing is supported. For more info, see [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs), and the [Direct3D 12 background processing spec](https://microsoft.github.io/DirectX-Specs/d3d/BackgroundProcessing.html).

## -struct-fields

### -field AdditionalShadingRatesSupported

Type: <b>[BOOL](/windows/desktop/winprog/windows-data-types)</b>

Indicates whether 2x4, 4x2, and 4x4 coarse pixel sizes are supported for single-sampled rendering; and whether coarse pixel size 2x4 is supported for 2x MSAA. `true` if those sizes are supported, otherwise `false`.

### -field PerPrimitiveShadingRateSupportedWithViewportIndexing

Type: <b>[BOOL](/windows/desktop/winprog/windows-data-types)</b>

Indicates whether the per-provoking-vertex (also known as per-primitive) rate can be used with more than one viewport. If so, then, in that case, that rate can be used when `SV_ViewportIndex` is written to. `true` if that rate can be used with more than one viewport, otherwise `false`.

### -field VariableShadingRateTier

Type: <b>[D3D12_VARIABLE_SHADING_RATE_TIER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)</b>

Indicates the shading rate tier.

### -field ShadingRateImageTileSize

Type: <b>[UINT](/windows/desktop/winprog/windows-data-types)</b>

Indicates the tile size of the screen-space image as a **UINT**.

### -field BackgroundProcessingSupported

Type: <b>[BOOL](/windows/desktop/winprog/windows-data-types)</b>

Indicates whether or not background processing is supported. `true` if background processing is supported, otherwise `false`. For more info, see the [Direct3D 12 background processing spec](https://microsoft.github.io/DirectX-Specs/d3d/BackgroundProcessing.html).

## -remarks

## -see-also

* [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
* [Direct3D 12 background processing spec](https://microsoft.github.io/DirectX-Specs/d3d/BackgroundProcessing.html)
