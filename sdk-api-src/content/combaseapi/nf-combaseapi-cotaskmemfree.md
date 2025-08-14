---
UID: NF:combaseapi.CoTaskMemFree
title: CoTaskMemFree function (combaseapi.h)
description: Frees a block of task memory previously allocated through a call to the CoTaskMemAlloc or CoTaskMemRealloc function.
helpviewer_keywords: ["CoTaskMemFree","CoTaskMemFree function [COM]","_com_CoTaskMemFree","com.cotaskmemfree","combaseapi/CoTaskMemFree"]
old-location: com\cotaskmemfree.htm
tech.root: com
ms.assetid: 3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7
ms.date: 12/05/2018
ms.keywords: CoTaskMemFree, CoTaskMemFree function [COM], _com_CoTaskMemFree, com.cotaskmemfree, combaseapi/CoTaskMemFree
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoTaskMemFree
 - combaseapi/CoTaskMemFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoTaskMemFree
---

# CoTaskMemFree function


## -description

Frees a block of task memory previously allocated through a call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc">CoTaskMemRealloc</a> function.

## -parameters

### -param pv [in, optional]

A pointer to the memory block to be freed. If this parameter is <b>NULL</b>, the function has no effect.

## -remarks

The <b>CoTaskMemFree</b> function uses the default OLE allocator.

The number of bytes freed equals the number of bytes that were originally allocated or reallocated. After the call, the memory block pointed to by pv is invalid and can no longer be used.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc">CoTaskMemRealloc</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>