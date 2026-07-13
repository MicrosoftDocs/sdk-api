---
UID: NF:memoryapi.QueryMemoryResourceNotification
title: QueryMemoryResourceNotification function (memoryapi.h)
description: Retrieves the state of the specified memory resource object.
helpviewer_keywords: ["QueryMemoryResourceNotification","QueryMemoryResourceNotification function","_win32_querymemoryresourcenotification","base.querymemoryresourcenotification","winbase/QueryMemoryResourceNotification"]
old-location: base\querymemoryresourcenotification.htm
tech.root: base
ms.assetid: 95a38b97-7fae-4ec6-aa9e-cc800d40594b
ms.date: 12/05/2018
ms.keywords: QueryMemoryResourceNotification, QueryMemoryResourceNotification function, _win32_querymemoryresourcenotification, base.querymemoryresourcenotification, winbase/QueryMemoryResourceNotification
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - QueryMemoryResourceNotification
 - memoryapi/QueryMemoryResourceNotification
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
 - QueryMemoryResourceNotification
---

# QueryMemoryResourceNotification function


## -description

Retrieves the state of the specified memory resource object.

## -parameters

### -param ResourceNotificationHandle [in]

A handle to a memory resource notification object. The 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-creatememoryresourcenotification">CreateMemoryResourceNotification</a> function returns this handle.

### -param ResourceState [out]

The memory pointed to by this parameter receives the state of the memory resource notification object. The value of this parameter is set to <b>TRUE</b> if the specified memory condition exists, and  <b>FALSE</b> if the specified memory condition does not exist.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. For more error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Unlike the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>, 
<b>QueryMemoryResourceNotification</b> does not block the calling thread. Therefore, it is an efficient way to check the state of physical memory before proceeding with an operation.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0501 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-creatememoryresourcenotification">CreateMemoryResourceNotification</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>