---
UID: NF:threadpoolapiset.QueryThreadpoolStackInformation
title: QueryThreadpoolStackInformation function (threadpoolapiset.h)
description: Retrieves the stack reserve and commit sizes for threads in the specified thread pool.
helpviewer_keywords: ["QueryThreadpoolStackInformation","QueryThreadpoolStackInformation function","base.querythreadpoolstackinformation","threadpoolapiset/QueryThreadpoolStackInformation","winbase/QueryThreadpoolStackInformation"]
old-location: base\querythreadpoolstackinformation.htm
tech.root: backup
ms.assetid: 1669dfa7-75bf-4776-bba7-7d03a084a32c
ms.date: 12/05/2018
ms.keywords: QueryThreadpoolStackInformation, QueryThreadpoolStackInformation function, base.querythreadpoolstackinformation, threadpoolapiset/QueryThreadpoolStackInformation, winbase/QueryThreadpoolStackInformation
req.header: threadpoolapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryThreadpoolStackInformation
 - threadpoolapiset/QueryThreadpoolStackInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - QueryThreadpoolStackInformation
---

# QueryThreadpoolStackInformation function


## -description

Retrieves the stack reserve and commit sizes for threads in the specified thread pool.

## -parameters

### -param ptpp [in]

A pointer to a <b>TP_POOL</b> structure that specifies the thread pool. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this pointer.

### -param ptpsi [out]

A pointer to a <b>TP_POOL_STACK_INFORMATION</b> structure that receives the stack reserve and commit size.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT to _WIN32_WINNT_WIN7. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation">SetThreadpoolStackInformation</a>