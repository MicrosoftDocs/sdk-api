---
UID: NF:winbase.UmsThreadYield
title: UmsThreadYield function (winbase.h)
description: Yields control to the user-mode scheduling (UMS) scheduler thread on which the calling UMS worker thread is running.
helpviewer_keywords: ["UmsThreadYield","UmsThreadYield function","base.umsthreadyield","winbase/UmsThreadYield"]
old-location: base\umsthreadyield.htm
tech.root: backup
ms.assetid: d7c94ed5-9536-4c39-8658-27e4237cc9ba
ms.date: 12/05/2018
ms.keywords: UmsThreadYield, UmsThreadYield function, base.umsthreadyield, winbase/UmsThreadYield
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - UmsThreadYield
 - winbase/UmsThreadYield
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - UmsThreadYield
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# UmsThreadYield function


## -description

Yields control to the user-mode scheduling (UMS) scheduler thread on which the calling UMS worker thread is running.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param SchedulerParam [in]

A parameter to pass to the scheduler thread's <a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> function.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A UMS worker thread calls the <b>UmsThreadYield</b> function to cooperatively yield control to the UMS scheduler thread on which the worker thread is running. If a UMS worker thread never calls <b>UmsThreadYield</b>, the worker thread runs until it either blocks or is terminated.

When control switches to the UMS scheduler thread, the system calls the associated scheduler entry point function with the reason <b>UmsSchedulerThreadYield</b> and the <i>ScheduleParam</i> parameter specified by the worker thread in the <b>UmsThreadYield</b> call. 

The application's scheduler is responsible for rescheduling the worker thread.

## -see-also

<a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a>
