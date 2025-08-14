---
UID: NF:combaseapi.CoGetMalloc
title: CoGetMalloc function (combaseapi.h)
description: Retrieves a pointer to the default OLE task memory allocator (which supports the system implementation of the IMalloc interface) so applications can call its methods to manage memory.
helpviewer_keywords: ["CoGetMalloc","CoGetMalloc function [COM]","_com_CoGetMalloc","com.cogetmalloc","combaseapi/CoGetMalloc"]
old-location: com\cogetmalloc.htm
tech.root: com
ms.assetid: d1d09fbe-ca5c-4480-b807-3afcc043ccb9
ms.date: 12/05/2018
ms.keywords: CoGetMalloc, CoGetMalloc function [COM], _com_CoGetMalloc, com.cogetmalloc, combaseapi/CoGetMalloc
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - CoGetMalloc
 - combaseapi/CoGetMalloc
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
 - CoGetMalloc
---

# CoGetMalloc function


## -description

Retrieves a pointer to the default OLE task memory allocator (which supports the system implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface) so applications can call its methods to manage memory.

## -parameters

### -param dwMemContext [in]

This parameter must be 1.

### -param ppMalloc [out]

The address of an <b>IMalloc*</b> pointer variable that receives the interface pointer to the memory allocator.

## -returns

This function can return the standard return values S_OK, E_INVALIDARG, and E_OUTOFMEMORY.

## -remarks

The pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface pointer received through the <i>ppMalloc</i> parameter cannot be used from a remote process; each process must have its own allocator.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>