---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS2
title: D3D12_FEATURE_DATA_D3D12_OPTIONS2 (d3d12.h)
description: Indicates the level of support that the adapter provides for depth-bounds tests and programmable sample positions.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS2","D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure","d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS2","direct3d12.d3d12_feature_data_d3d12_options2"]
old-location: direct3d12\d3d12_feature_data_d3d12_options2.htm
tech.root: direct3d12
ms.assetid: E45DA471-E0A9-47BF-8AE5-4B8BA4B38337
ms.date: 08/10/2022
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS2, D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS2, direct3d12.d3d12_feature_data_d3d12_options2
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS2
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS2
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS2
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure


## -description

Indicates the level of support that the adapter provides for depth-bounds tests and programmable sample positions.

## -struct-fields

### -field DepthBoundsTestSupported

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_Out_</code>

On return, contains true if depth-bounds tests are supported; otherwise, false.

### -field ProgrammableSamplePositionsTier

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_Out_</code>

On return, contains a value that indicates the level of support offered for programmable sample positions.

## -remarks

Use this structure with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a> to determine the level of support offered for the optional Depth-bounds test and programmable sample positions features.

See the enumeration constant D3D12_FEATURE_D3D12_OPTIONS2 in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>