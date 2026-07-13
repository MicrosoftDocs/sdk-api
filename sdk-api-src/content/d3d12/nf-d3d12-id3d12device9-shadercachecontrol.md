---
UID: NF:d3d12.ID3D12Device9.ShaderCacheControl
title: ID3D12Device9::ShaderCacheControl
description: Modifies the behavior of caches used internally by Direct3D or by the driver.
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
 - ID3D12Device9::ShaderCacheControl
f1_keywords:
 - ID3D12Device9::ShaderCacheControl
 - d3d12/ID3D12Device9::ShaderCacheControl
dev_langs:
 - c++
---

## -description

Modifies the behavior of caches used internally by Direct3D or by the driver. **ShaderCacheControl** may be used only in developer mode.

## -parameters

### -param Kinds

Type: **[D3D12_SHADER_CACHE_KIND_FLAGS](ne-d3d12-d3d12_shader_cache_kind_flags.md)**

The caches to modify. Any one of these caches may or may not exist.

### -param Control

Type: **[D3D12_SHADER_CACHE_CONTROL_FLAGS](ne-d3d12-d3d12_shader_cache_control_flags.md)**

The way in which to modify the caches. You can't pass both **DISABLE** and **ENABLE** at the same time; and you must pass at least one flag.

## -returns

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
