---
UID: NF:threadpoolapiset.WaitForThreadpoolTimerCallbacks
title: WaitForThreadpoolTimerCallbacks function (threadpoolapiset.h)
description: Waits for outstanding timer callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
helpviewer_keywords: ["WaitForThreadpoolTimerCallbacks","WaitForThreadpoolTimerCallbacks function","base.waitforthreadpooltimercallbacks","threadpoolapiset/WaitForThreadpoolTimerCallbacks","winbase/WaitForThreadpoolTimerCallbacks"]
old-location: base\waitforthreadpooltimercallbacks.htm
tech.root: backup
ms.assetid: 511488b8-9e92-47b9-8b3c-7ece9d9f996c
ms.date: 12/05/2018
ms.keywords: WaitForThreadpoolTimerCallbacks, WaitForThreadpoolTimerCallbacks function, base.waitforthreadpooltimercallbacks, threadpoolapiset/WaitForThreadpoolTimerCallbacks, winbase/WaitForThreadpoolTimerCallbacks
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
 - WaitForThreadpoolTimerCallbacks
 - threadpoolapiset/WaitForThreadpoolTimerCallbacks
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
 - WaitForThreadpoolTimerCallbacks
---

# WaitForThreadpoolTimerCallbacks function


## -description

Waits for outstanding timer callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.

## -parameters

### -param pti [in, out]

A pointer to a <b>TP_TIMER</b> structure that defines the timer object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a> function returns this pointer.

### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset">IsThreadpoolTimerSet</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>