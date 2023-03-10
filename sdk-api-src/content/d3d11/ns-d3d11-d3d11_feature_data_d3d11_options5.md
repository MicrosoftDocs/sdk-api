---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D11_OPTIONS5
title: D3D11_FEATURE_DATA_D3D11_OPTIONS5
description: Describes the level of support for shared resources in the current graphics driver.
ms.date: 05/27/2020
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D11_OPTIONS5","D3D11_FEATURE_DATA_D3D11_OPTIONS5 structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS5","direct3d11.d3d11_feature_data_d3d11_options4"]
tech.root: direct3d11
req.construct-type: structure
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D3D11_FEATURE_DATA_D3D11_OPTIONS5
req.redist: 
f1_keywords:
 - D3D11_FEATURE_DATA_D3D11_OPTIONS5
 - d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS5
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_FEATURE_DATA_D3D11_OPTIONS5
---

## -description

Describes the level of support for shared resources in the current graphics driver.

## -struct-fields

### -field SharedResourceTier

Type: **[D3D11_SHARED_RESOURCE_TIER](./ne-d3d11-d3d11_shared_resource_tier.md)**

The level of support for shared resources in the current graphics driver.

## -remarks

Use this structure with the **D3D11_FEATURE_D3D11_OPTIONS5** member of [D3D11_FEATURE](./ne-d3d11-d3d11_feature.md).

## -see-also

[Direct3D 11 core structures](/windows/win32/direct3d11/d3d11-graphics-reference-d3d11-core-structures)
