---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS12
title: D3D12_FEATURE_DATA_D3D12_OPTIONS12
description: Indicates whether or not Enhanced Barriers are supported.
tech.root: direct3d12
ms.date: 10/28/2022
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
req.target-min-winverclnt: Windows 11, version 22H2; or DirectX 12 Agility SDK 1.6 or later
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS12
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS12
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS12
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS12
prerelease: false
---

## -description

Indicates whether or not Enhanced Barriers are supported.

## -struct-fields

### -field MSPrimitivesPipelineStatisticIncludesCulledPrimitives

Type: \_Out\_ **[D3D12_TRI_STATE](ne-d3d12-d3d12_tri_state.md)**

TBD

### -field EnhancedBarriersSupported

Type: \_Out\_ **[BOOL](/windows/win32/winprog/windows-data-types)**

Indicates whether or not Enhanced Barriers are supported. `true` if supported, otherwise `false`.

Enhanced Barriers is not currently a hardware or driver requirement. So before using command list Barrier APIs, or resource creation APIs using the *InitialLayout* parameter, you must check for optional driver support via *EnhancedBarriersSupported*.

Requires the DirectX 12 Agility SDK 1.6 or later; otherwise, the value is always `FALSE`.

### -field RelaxedFormatCastingSupported

Type: \_Out\_ **[BOOL](/windows/win32/winprog/windows-data-types)**

Technically used to indicate support for the functionality that enables integer aliasing.

Requires the DirectX 12 Agility SDK 1.6 or later; otherwise, the value is always `FALSE`.

## -remarks

## -see-also
