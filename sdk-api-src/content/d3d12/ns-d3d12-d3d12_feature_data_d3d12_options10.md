---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS10
title: D3D12_FEATURE_DATA_D3D12_OPTIONS10
description: Indicates whether or not the SUM combiner can be used, and whether or not *SV_ShadingRate* can be set from a mesh shader.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS10
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS10
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS10
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS10
prerelease: false
---

## -description

Indicates whether or not the SUM combiner can be used, and whether or not *SV_ShadingRate* can be set from a mesh shader.

## -struct-fields

### -field VariableRateShadingSumCombinerSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not the SUM combiner can be used (this relates to [variable-rate shading](/windows/desktop/direct3d12/vrs) Tier 2). `true` if it can, otherwise `false`.

### -field MeshShaderPerPrimitiveShadingRateSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not *SV_ShadingRate* can be set from a mesh shader (this relates to [variable-rate shading](/windows/desktop/direct3d12/vrs) Tier 2). `true` if it can, otherwise `false`.

## -remarks

## -see-also

* [Variable-rate shading (VRS)](/windows/desktop/direct3d12/vrs)
