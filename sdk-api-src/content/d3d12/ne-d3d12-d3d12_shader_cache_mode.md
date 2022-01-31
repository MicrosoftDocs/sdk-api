---
UID: NE:d3d12.D3D12_SHADER_CACHE_MODE
title: D3D12_SHADER_CACHE_MODE
description: Defines constants that specify a shader cache's mode.
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
 - D3D12_SHADER_CACHE_MODE
 - d3d12/D3D12_SHADER_CACHE_MODE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADER_CACHE_MODE
---

## -description

Defines constants that specify a shader cache's mode.

## -enum-fields

### -field D3D12_SHADER_CACHE_MODE_MEMORY:0

Specifies that there's no backing file for this cache. All stores are discarded when the session object is destroyed.

### -field D3D12_SHADER_CACHE_MODE_DISK

Specifies that the session is backed by files on disk that persist from run to run unless cleared. For ways to clear a disk cache, see [ID3D12ShaderCacheSession::SetDeleteOnDestroy](nf-d3d12-id3d12shadercachesession-setdeleteondestroy.md).

## -remarks

## -see-also

* [ID3D12ShaderCacheSession::SetDeleteOnDestroy](nf-d3d12-id3d12shadercachesession-setdeleteondestroy.md)
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
