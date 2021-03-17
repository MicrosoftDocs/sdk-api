---
UID: NS:d3d12.D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS
title: D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS (d3d12.h)
description: Describes the multi-sampling image quality levels for a given format and sample count.
helpviewer_keywords: ["D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS","D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS structure","d3d12/D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS","direct3d12.d3d12_feature_data_multisample_quality_levels"]
old-location: direct3d12\d3d12_feature_data_multisample_quality_levels.htm
tech.root: direct3d12
ms.assetid: F3ECEF7C-F4A4-4134-9671-21AE488D8183
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS, D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS structure, d3d12/D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS, direct3d12.d3d12_feature_data_multisample_quality_levels
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
req.typenames: D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS
 - d3d12/D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS
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
 - D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS
---

# D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS structure


## -description

Describes the multi-sampling image quality levels for a given format and sample count.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the format to return info about.

### -field SampleCount

The number of multi-samples per pixel to return info about.

### -field Flags

Flags to control quality levels, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags">D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS</a> enumeration constants.
            The resulting value specifies options for determining quality levels.

### -field NumQualityLevels

The number of quality levels.

## -remarks

See <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>