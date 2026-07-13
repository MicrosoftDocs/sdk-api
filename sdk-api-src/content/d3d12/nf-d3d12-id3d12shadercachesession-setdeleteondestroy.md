---
UID: NF:d3d12.ID3D12ShaderCacheSession.SetDeleteOnDestroy
title: ID3D12ShaderCacheSession::SetDeleteOnDestroy
description: When all cache session objects corresponding to a given cache are destroyed, the cache is cleared.
tech.root: direct3d12
ms.date: 08/10/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12ShaderCacheSession::SetDeleteOnDestroy
f1_keywords:
 - ID3D12ShaderCacheSession::SetDeleteOnDestroy
 - d3d12/ID3D12ShaderCacheSession::SetDeleteOnDestroy
dev_langs:
 - c++
---

## -description

When all cache session objects corresponding to a given cache are destroyed, the cache is cleared.

See **Remarks** for the ways in which a disk cache can be cleared.

## -remarks

A disk cache can be cleared in one of the following ways.

* Explicitly, by calling **SetDeleteOnDestroy** on the session object, and then releasing the session.
* Explicitly, in developer mode, by calling [ID3D12Device9::ShaderCacheControl](nf-d3d12-id3d12device9-shadercachecontrol.md) with [D3D12_SHADER_CACHE_KIND_FLAG_APPLICATION_MANAGED](ne-d3d12-d3d12_shader_cache_kind_flags.md).
* Implicitly, by creating a session object with a version that doesn't match the version used to create it.
* Externally, by the disk cleanup utility enumerating it and clearing it. This won't happen for caches created with the [D3D12_SHADER_CACHE_FLAG_USE_WORKING_DIR](ne-d3d12-d3d12_shader_cache_flags.md) flag.
* Manually, by deleting the files (`*.idx`, `*.val`, and `*.lock`) stored on disk for [D3D12_SHADER_CACHE_FLAG_USE_WORKING_DIR](ne-d3d12-d3d12_shader_cache_flags.md) caches. Your application shouldn't attempt to do this for caches stored outside of the working directory.

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
