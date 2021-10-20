---
UID: NS:d3d12.D3D12_SHADER_CACHE_SESSION_DESC
title: D3D12_SHADER_CACHE_SESSION_DESC
description: Describes a shader cache session.
tech.root: direct3d12
ms.date: 08/09/2021
req.construct-type: structure
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
req.typenames: D3D12_SHADER_CACHE_SESSION_DESC
req.redist: 
f1_keywords:
 - D3D12_SHADER_CACHE_SESSION_DESC
 - d3d12/D3D12_SHADER_CACHE_SESSION_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SHADER_CACHE_SESSION_DESC
---

## -description

Describes a shader cache session.

## -struct-fields

### -field Identifier

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

A unique identifier to give to this specific cache. Caches with different identifiers are stored side by side. Caches with the same identifier are shared across all sessions in the same process. Creating a disk cache with the same identifier as an already-existing cache opens that cache, unless the **Version** doesn't matches. In that case, if there are no other sessions open to that cache, it is cleared and re-created. If there are existing sessions, then [ID3D12Device9::CreateShaderCacheSession](nf-d3d12-id3d12device9-createshadercachesession.md) returns **DXGI_ERROR_ALREADY_EXISTS**.

### -field Mode

Type: **[D3D12_SHADER_CACHE_MODE](ne-d3d12-d3d12_shader_cache_mode.md)**

Specifies the kind of cache.

### -field Flags

Type: **[D3D12_SHADER_CACHE_FLAGS](ne-d3d12-d3d12_shader_cache_flags.md)**

Modifies the behavior of the cache.

### -field MaximumInMemoryCacheSizeBytes

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

For in-memory caches, this is the only storage available. For disk caches, all entries that are stored or found are temporarily stored in memory, until evicted by newer entries. This value determines the size of that temporary storage. Defaults to 1KB.

### -field MaximumInMemoryCacheEntries

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

Specifies how many entries can be stored in memory. Defaults to 128.

### -field MaximumValueFileSizeBytes

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

For disk caches, controls the maximum file size. Defaults to 128MB.

### -field Version

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

Can be used to implicitly clear caches when an application or component update is done. If the version doesn't match the version stored in the cache, then it will be wiped and re-created.

## -remarks

## -see-also

* [ID3D12Device9::CreateShaderCacheSession](nf-d3d12-id3d12device9-createshadercachesession.md)
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
