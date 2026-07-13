---
UID: NF:memoryapi.GetLargePageMinimum
title: GetLargePageMinimum function (memoryapi.h)
description: Retrieves the minimum size of a large page.
helpviewer_keywords: ["GetLargePageMinimum","GetLargePageMinimum function","base.getlargepageminimum","winbase/GetLargePageMinimum"]
old-location: base\getlargepageminimum.htm
tech.root: base
ms.assetid: ccde687d-ee8f-4668-93c1-a1fece86c2f6
ms.date: 12/05/2018
ms.keywords: GetLargePageMinimum, GetLargePageMinimum function, base.getlargepageminimum, winbase/GetLargePageMinimum
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetLargePageMinimum
 - memoryapi/GetLargePageMinimum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - GetLargePageMinimum
---

# GetLargePageMinimum function


## -description

Retrieves the minimum size of a large page.



## -returns

If the processor supports large pages, the return value is the minimum size of a large page.

If the processor does not support large pages, the return value is zero.

## -remarks

The minimum large page size varies, but it is typically 2 MB or greater.

## -see-also

<a href="/windows/desktop/Memory/large-page-support">Large Page Support</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
