---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS4
title: D3D12_FEATURE_DATA_D3D12_OPTIONS4
description: Indicates the level of support for 64KB-aligned MSAA textures, cross-API sharing, and native 16-bit shader operations.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS4"]
tech.root: direct3d12
ms.date: 05/20/2019
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS4
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS4
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS4
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS4
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS4
---

## -description

Indicates the level of support for 64KB-aligned MSAA textures, cross-API sharing, and native 16-bit shader operations.

## -struct-fields

### -field MSAA64KBAlignedTextureSupported

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether 64KB-aligned MSAA textures are supported.

### -field SharedResourceCompatibilityTier

Type: **[D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier)**

Indicates the tier of cross-API sharing support.

### -field Native16BitShaderOpsSupported

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates native 16-bit shader operations are supported. These operations require shader model 6_2. For more information, see the [16-Bit Scalar Types](https://github.com/microsoft/DirectXShaderCompiler/wiki/16-Bit-Scalar-Types) HLSL reference.

## -remarks

## -see-also

