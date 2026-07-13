---
UID: NF:winbase.GetUmsSystemThreadInformation
title: GetUmsSystemThreadInformation function (winbase.h)
description: Queries whether the specified thread is a UMS scheduler thread, a UMS worker thread, or a non-UMS thread.
helpviewer_keywords: ["GetUmsSystemThreadInformation","GetUmsSystemThreadInformation function","base.getumssystemthreadinformation","winbase/GetUmsSystemThreadInformation"]
old-location: base\getumssystemthreadinformation.htm
tech.root: backup
ms.assetid: 7c8347b6-6546-4ea9-9b2a-11794782f482
ms.date: 12/05/2018
ms.keywords: GetUmsSystemThreadInformation, GetUmsSystemThreadInformation function, base.getumssystemthreadinformation, winbase/GetUmsSystemThreadInformation
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps only],Windows 7 (64-bit only) and Windows Server 2008 R2 with KB977165 installed
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps only]
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
 - GetUmsSystemThreadInformation
 - winbase/GetUmsSystemThreadInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - GetUmsSystemThreadInformation
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# GetUmsSystemThreadInformation function

## -description

Queries whether the specified thread is a UMS scheduler thread, a UMS worker thread, or a non-UMS thread.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param ThreadHandle [in]

A handle to a thread. The thread handle must have the THREAD_QUERY_INFORMATION access right. For more information, see [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).

### -param SystemThreadInfo [in, out]

A pointer to a [UMS_SYSTEM_THREAD_INFORMATION](/windows/desktop/api/winbase/ns-winbase-ums_system_thread_information) structure that receives information about the specified thread.

The caller must initialize the `UmsVersion` member before calling.

## -returns

If the function fails, the return value is zero.

To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The **GetUmsSystemThreadInformation** function is intended for use in debuggers, troubleshooting tools, and profiling applications. For example, thread-isolated tracing or single-stepping through instructions might involve suspending all other threads in the process. However, if the thread to be traced is a UMS worker thread, suspending UMS scheduler threads might cause a deadlock because a UMS worker thread requires the intervention of a UMS scheduler thread in order to run. A debugger can call **GetUmsSystemThreadInformation** for each thread that it might suspend to determine the kind of thread, and then suspend it or not as needed for the code being debugged.
