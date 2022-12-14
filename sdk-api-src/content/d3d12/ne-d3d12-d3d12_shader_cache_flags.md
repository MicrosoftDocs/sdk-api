---
UID: NE:d3d12.D3D12_SHADER_CACHE_FLAGS
title: D3D12_SHADER_CACHE_FLAGS
description: Defines constants that specify shader cache flags.
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
 - D3D12_SHADER_CACHE_FLAGS
 - d3d12/D3D12_SHADER_CACHE_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADER_CACHE_FLAGS
---

## -description

Defines constants that specify shader cache flags.

## -enum-fields

### -field D3D12_SHADER_CACHE_FLAG_NONE:0

Specifies no flag.

### -field D3D12_SHADER_CACHE_FLAG_DRIVER_VERSIONED:0x1

Specifies that the cache is implicitly versioned by the driver being used. For multi-GPU systems, a cache created this way is stored side by side for each adapter on which the application runs. The *Version* field in the [D3D12_SHADER_CACHE_SESSION_DESC](ns-d3d12-d3d12_shader_cache_session_desc.md) struct (the cache description) is used as an additional constraint.

### -field D3D12_SHADER_CACHE_FLAG_USE_WORKING_DIR:0x2

By default, caches are stored in temporary storage, and can be cleared by disk cleanup. This constant (not valid for UWP apps) specifies that the cache is instead stored in the current working directory.

## -remarks

## -see-also

* [D3D12_SHADER_CACHE_SESSION_DESC](ns-d3d12-d3d12_shader_cache_session_desc.md)
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
