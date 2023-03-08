---
UID: NE:d3d12.D3D12_SHADER_CACHE_KIND_FLAGS
title: D3D12_SHADER_CACHE_KIND_FLAGS
description: Defines constants that specify a kind of shader cache.
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
 - D3D12_SHADER_CACHE_KIND_FLAGS
 - d3d12/D3D12_SHADER_CACHE_KIND_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADER_CACHE_KIND_FLAGS
---

## -description

Defines constants that specify a kind of shader cache.

## -enum-fields

### -field D3D12_SHADER_CACHE_KIND_FLAG_IMPLICIT_D3D_CACHE_FOR_DRIVER:0x1

Specifies a cache that's managed by Direct3D 12 to store driver compilations of application shaders.

### -field D3D12_SHADER_CACHE_KIND_FLAG_IMPLICIT_D3D_CONVERSIONS:0x2

Specifies a cache that's used to store Direct3D 12's conversions of one shader type to another (for example, DXBC shaders to DXIL shaders).

### -field D3D12_SHADER_CACHE_KIND_FLAG_IMPLICIT_DRIVER_MANAGED:0x4

Specifies a cache that's managed by the driver. Operations for this cache are hints.

### -field D3D12_SHADER_CACHE_KIND_FLAG_APPLICATION_MANAGED:0x8

Specifies all shader cache sessions created by the [ID3D12Device9::CreateShaderCacheSession](nf-d3d12-id3d12device9-createshadercachesession.md) method. Requests to **CLEAR** with this flag apply to all currently active application cache sessions, as well as on-disk caches created without [D3D12_SHADER_CACHE_FLAG_USE_WORKING_DIR](ne-d3d12-d3d12_shader_cache_flags.md).

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
