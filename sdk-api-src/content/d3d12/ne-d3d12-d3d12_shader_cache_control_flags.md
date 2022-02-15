---
UID: NE:d3d12.D3D12_SHADER_CACHE_CONTROL_FLAGS
title: D3D12_SHADER_CACHE_CONTROL_FLAGS
description: Defines constants that specify shader cache control options.
tech.root: direct3d12
ms.date: 08/09/2021
req.construct-type: enumeration
req.header: d3d12.h
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
req.redist: 
f1_keywords:
 - D3D12_SHADER_CACHE_CONTROL_FLAGS
 - d3d12/D3D12_SHADER_CACHE_CONTROL_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADER_CACHE_CONTROL_FLAGS
---

## -description

Defines constants that specify shader cache control options.

## -enum-fields

### -field D3D12_SHADER_CACHE_CONTROL_FLAG_DISABLE:0x1

Specifies that the cache shouldn't be used to look up data, and shouldn't have new data stored in it. Attempts to use/create a cache while it's disabled result in **DXGI_ERROR_NOT_CURRENTLY_AVAILABLE**.

### -field D3D12_SHADER_CACHE_CONTROL_FLAG_ENABLE:0x2

Specfies that use of the cache should be resumed.

### -field D3D12_SHADER_CACHE_CONTROL_FLAG_CLEAR:0x4

Specfies that any existing contents of the cache should be deleted.

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
