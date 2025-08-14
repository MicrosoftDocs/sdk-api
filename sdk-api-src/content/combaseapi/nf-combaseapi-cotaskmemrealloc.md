---
UID: NF:combaseapi.CoTaskMemRealloc
title: CoTaskMemRealloc function (combaseapi.h)
description: Changes the size of a previously allocated block of task memory.
helpviewer_keywords: ["CoTaskMemRealloc","CoTaskMemRealloc function [COM]","_com_CoTaskMemRealloc","com.cotaskmemrealloc","combaseapi/CoTaskMemRealloc"]
old-location: com\cotaskmemrealloc.htm
tech.root: com
ms.assetid: 83014a3e-198d-4b4b-91aa-0c0804c8e1bf
ms.date: 12/05/2018
ms.keywords: CoTaskMemRealloc, CoTaskMemRealloc function [COM], _com_CoTaskMemRealloc, com.cotaskmemrealloc, combaseapi/CoTaskMemRealloc
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
 - CoTaskMemRealloc
 - combaseapi/CoTaskMemRealloc
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
 - CoTaskMemRealloc
---

# CoTaskMemRealloc function


## -description

Changes the size of a previously allocated block of task memory.

## -parameters

### -param pv [in, optional]

A pointer to the memory block to be reallocated. This parameter can be <b>NULL</b>, as discussed in Remarks.

### -param cb [in]

The size of the memory block to be reallocated, in bytes. This parameter can be 0, as discussed in Remarks.

## -returns

If the function succeeds, it returns the reallocated memory block. Otherwise, it returns <b>NULL</b>.

## -remarks

This function changes the size of a previously allocated memory block in the same way that <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a> does. It is not necessary to call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a> function to get a pointer to the OLE allocator before calling <b>CoTaskMemRealloc</b>.

The <i>pv</i> parameter points to the beginning of the memory block. If <i>pv</i> is <b>NULL</b>, <b>CoTaskMemRealloc</b> allocates a new memory block in the same way as the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function. If <i>pv</i> is not <b>NULL</b>, it should be a pointer returned by a prior call to <b>CoTaskMemAlloc</b>.

The <i>cb</i> parameter specifies the size of the new block. The contents of the block are unchanged up to the shorter of the new and old sizes, although the new block can be in a different location. Because the new block can be in a different memory location, the pointer returned by <b>CoTaskMemRealloc</b> is not guaranteed to be the pointer passed through the <i>pv</i> argument. If <i>pv</i> is not <b>NULL</b> and <i>cb</i> is 0, then the memory pointed to by <i>pv</i> is freed.

<b>CoTaskMemRealloc</b> returns a void pointer to the reallocated (and possibly moved) memory block. The return value is <b>NULL</b> if the size is 0 and the buffer argument is not <b>NULL</b>, or if there is not enough memory available to expand the block to the specified size. In the first case, the original block is freed; in the second case, the original block is unchanged.

The storage space pointed to by the return value is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than <b>void</b>, use a type cast on the return value.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>