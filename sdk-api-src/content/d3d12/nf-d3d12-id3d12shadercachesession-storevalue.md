---
UID: NF:d3d12.ID3D12ShaderCacheSession.StoreValue
title: ID3D12ShaderCacheSession::StoreValue
description: Adds an entry to the cache.
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
 - ID3D12ShaderCacheSession::StoreValue
f1_keywords:
 - ID3D12ShaderCacheSession::StoreValue
 - d3d12/ID3D12ShaderCacheSession::StoreValue
dev_langs:
 - c++
---

## -description

Adds an entry to the cache.

## -parameters

### -param pKey

Type: \_In\_reads\_bytes\_(KeySize) **const void \***

The key of the entry to add.

### -param KeySize

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The size of the key, in bytes.

### -param pValue

Type: \_In\_reads\_bytes\_(ValueSize) **void \***

A pointer to a memory block containing the entry to add.

### -param ValueSize

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The size of the entry to add, in bytes.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
| DXGI_ERROR_ALREADY_EXISTS | There's an entry with the same key. |
| DXGI_ERROR_CACHE_HASH_COLLISION | There's an entry with the same hash as the provided key, but the key doesn't match. |
| DXGI_ERROR_CACHE_FULL | Adding this entry would cause the cache to become larger than its maximum size. |

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
