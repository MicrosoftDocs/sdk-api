---
UID: NF:d3d12.ID3D12ShaderCacheSession.FindValue
title: ID3D12ShaderCacheSession::FindValue
description: Looks up an entry in the cache whose key exactly matches the provided key.
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
 - ID3D12ShaderCacheSession::FindValue
f1_keywords:
 - ID3D12ShaderCacheSession::FindValue
 - d3d12/ID3D12ShaderCacheSession::FindValue
dev_langs:
 - c++
---

## -description

Looks up an entry in the cache whose key exactly matches the provided key.

Call the function twice. The first time to retrieve the value's size, and the second time to retrieve the data. In-memory temporary storage makes this calling pattern performant.

## -parameters

### -param pKey

Type: \_In\_reads\_bytes\_(KeySize) **const void \***

The key of the entry to look up.

### -param KeySize

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The size of the key, in bytes.

### -param pValue

Type: \_Out\_writes\_bytes\_(*pValueSize) **void \***

A pointer to a memory block that receives the cached entry.

### -param pValueSize

Type: \_Inout\_ **[UINT](/windows/win32/winprog/windows-data-types)\***

A pointer to a **UINT** that receives the size of the cached entry, in bytes.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
| DXGI_ERROR_CACHE_HASH_COLLISION | There's an entry with the same hash as the provided key, but the key doesn't exactly match. |
| DXGI_ERROR_NOT_FOUND | The entry isn't present. |

## -remarks

## -see-also
* [D3D12 shader cache APIs](https://microsoft.github.io/DirectX-Specs/d3d/ShaderCache.html)
