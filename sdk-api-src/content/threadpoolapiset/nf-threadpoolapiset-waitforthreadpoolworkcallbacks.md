---
UID: NF:threadpoolapiset.WaitForThreadpoolWorkCallbacks
title: WaitForThreadpoolWorkCallbacks function (threadpoolapiset.h)
description: Waits for outstanding work callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
helpviewer_keywords: ["WaitForThreadpoolWorkCallbacks","WaitForThreadpoolWorkCallbacks function","base.waitforthreadpoolworkcallbacks","threadpoolapiset/WaitForThreadpoolWorkCallbacks","winbase/WaitForThreadpoolWorkCallbacks"]
old-location: base\waitforthreadpoolworkcallbacks.htm
tech.root: backup
ms.assetid: 97c16892-d6ef-4216-ac79-344e83ab35bc
ms.date: 12/05/2018
ms.keywords: WaitForThreadpoolWorkCallbacks, WaitForThreadpoolWorkCallbacks function, base.waitforthreadpoolworkcallbacks, threadpoolapiset/WaitForThreadpoolWorkCallbacks, winbase/WaitForThreadpoolWorkCallbacks
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - WaitForThreadpoolWorkCallbacks
 - threadpoolapiset/WaitForThreadpoolWorkCallbacks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - WaitForThreadpoolWorkCallbacks
---

# WaitForThreadpoolWorkCallbacks function


## -description

Waits for outstanding work callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.

## -parameters

### -param pwk [in, out]

A pointer to a <b>TP_WORK</b> structure that defines the work object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a> function returns this pointer.

### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>