---
UID: NS:d3d11.D3D11_FEATURE_DATA_SHADER_CACHE
title: D3D11_FEATURE_DATA_SHADER_CACHE (d3d11.h)
description: Describes the level of shader caching supported in the current graphics driver. (D3D11_FEATURE_DATA_SHADER_CACHE)
helpviewer_keywords: ["D3D11_FEATURE_DATA_SHADER_CACHE","D3D11_FEATURE_DATA_SHADER_CACHE structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_SHADER_CACHE","direct3d11.d3d11_feature_data_shader_cache"]
old-location: direct3d11\d3d11_feature_data_shader_cache.htm
tech.root: direct3d11
ms.assetid: 45F1184E-0E82-4AF4-86F7-ED0E4C860026
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_SHADER_CACHE, D3D11_FEATURE_DATA_SHADER_CACHE structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_SHADER_CACHE, direct3d11.d3d11_feature_data_shader_cache
req.header: d3d11.h
req.include-header: D3d11_3.h
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
req.typenames: D3D11_FEATURE_DATA_SHADER_CACHE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_SHADER_CACHE
 - d3d11/D3D11_FEATURE_DATA_SHADER_CACHE
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
 - D3D11_FEATURE_DATA_SHADER_CACHE
---

# D3D11_FEATURE_DATA_SHADER_CACHE structure


## -description

Describes the level of shader caching supported in the current graphics driver.

## -struct-fields

### -field SupportFlags

Indicates the level of caching supported.

## -remarks

Use this structure with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">CheckFeatureSupport</a> to determine the level of support offered for the optional shader-caching features.

See the enumeration constant D3D11_FEATURE_SHADER_CACHE in the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a> enumeration.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
