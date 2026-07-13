---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS9
title: D3D12_FEATURE_DATA_D3D12_OPTIONS9
description: Indicates whether or not support exists for mesh shaders, values of *SV_RenderTargetArrayIndex* that are 8 or greater, typed resource 64-bit integer atomics, derivative and derivative-dependent texture sample operations, and the level of support for WaveMMA (wave_matrix) operations.
tech.root: direct3d12
ms.date: 07/21/2021
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS9
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS9
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS9
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS9
---

## -description

Indicates whether or not support exists for mesh shaders, values of *SV_RenderTargetArrayIndex* that are 8 or greater, typed resource 64-bit integer atomics, derivative and derivative-dependent texture sample operations, and the level of support for WaveMMA (wave_matrix) operations.

## -struct-fields

### -field MeshShaderPipelineStatsSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not mesh shaders are supported. `true` if supported, otherwise `false`.

### -field MeshShaderSupportsFullRangeRenderTargetArrayIndex

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not values of *SV_RenderTargetArrayIndex* that are 8 or greater are supported. `true` if supported, otherwise `false`.

### -field AtomicInt64OnTypedResourceSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not typed resource 64-bit integer atomics are supported. `true` if supported, otherwise `false`.

### -field AtomicInt64OnGroupSharedSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not 64-bit integer atomics are supported on `groupshared` variables. `true` if supported, otherwise `false`.

### -field DerivativesInMeshAndAmplificationShadersSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not derivative and derivative-dependent texture sample operations are supported. `true` if supported, otherwise `false`.

### -field WaveMMATier

Type: \_Out\_ **[D3D12_WAVE_MMA_TIER](ne-d3d12-d3d12_wave_mma_tier.md)**

Indicates the level of support for WaveMMA (wave_matrix) operations.

## -remarks

## -see-also

* [Mesh shader spec](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)
