---
UID: NE:d3d12.D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS
title: D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS (d3d12.h)
description: Specifies options for determining quality levels.
helpviewer_keywords: ["D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_NONE","D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_TILED_RESOURCE","D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS","D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS enumeration","d3d12/D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_NONE","d3d12/D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_TILED_RESOURCE","d3d12/D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS","direct3d12.d3d12_multisample_quality_level_flags"]
old-location: direct3d12\d3d12_multisample_quality_level_flags.htm
tech.root: direct3d12
ms.assetid: 78FBD851-879C-4C84-ACEA-58CF4ADE29A0
ms.date: 12/05/2018
ms.keywords: D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_NONE, D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_TILED_RESOURCE, D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS, D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS enumeration, d3d12/D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_NONE, d3d12/D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_TILED_RESOURCE, d3d12/D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS, direct3d12.d3d12_multisample_quality_level_flags
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
req.typenames: D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS
 - d3d12/D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS
---

# D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS enumeration


## -description

Specifies options for determining quality levels.

## -enum-fields

### -field D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_NONE:0

No options are supported.

### -field D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG_TILED_RESOURCE:0x1

The number of quality levels can be determined for tiled resources.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels">D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
