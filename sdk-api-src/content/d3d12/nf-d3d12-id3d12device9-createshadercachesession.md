---
UID: NF:d3d12.ID3D12Device9.CreateShaderCacheSession
title: ID3D12Device9::CreateShaderCacheSession
description: Creates an object that grants access to a shader cache, potentially opening an existing cache or creating a new one.
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
 - ID3D12Device9::CreateShaderCacheSession
f1_keywords:
 - ID3D12Device9::CreateShaderCacheSession
 - d3d12/ID3D12Device9::CreateShaderCacheSession
dev_langs:
 - c++
---

## -description

Creates an object that grants access to a shader cache, potentially opening an existing cache or creating a new one.

## -parameters

### -param pDesc

Type: \_In\_ **const [D3D12_SHADER_CACHE_SESSION_DESC](ns-d3d12-d3d12_shader_cache_session_desc.md)\***

A **D3D12_SHADER_CACHE_SESSION_DESC** structure describing the shader cache session to create.

### -param riid

Type: **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The globally unique identifier (GUID) for the shader cache session interface.

### -param ppvSession

Type: \_COM\_Outptr\_opt\_ **void\*\***

A pointer to a memory block that receives a pointer to the [ID3D12ShaderCacheSession](nn-d3d12-id3d12shadercachesession.md) interface for the shader cache session.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
| DXGI_ERROR_ALREADY_EXISTS | You tried to create a cache with an existing identifier. See [D3D12_SHADER_CACHE_SESSION_DESC::Identifier](ns-d3d12-d3d12_shader_cache_session_desc.md). |

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
