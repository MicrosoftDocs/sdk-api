---
UID: NF:processthreadsapi.GetThreadInformation
title: GetThreadInformation function (processthreadsapi.h)
description: Retrieves information about the specified thread.
helpviewer_keywords: ["GetThreadInformation","GetThreadInformation function","base.getthreadinformation","processthreadsapi/GetThreadInformation"]
old-location: base\getthreadinformation.htm
tech.root: backup
ms.assetid: b7996647-78ab-4f32-bcf6-41aa87d13bb8
ms.date: 01/21/2022
ms.keywords: GetThreadInformation, GetThreadInformation function, base.getthreadinformation, processthreadsapi/GetThreadInformation
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - GetThreadInformation
 - processthreadsapi/GetThreadInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadInformation
---

# GetThreadInformation function

## -description

Retrieves information about the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread. The handle must have THREAD_QUERY_INFORMATION access rights. For more information, see [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).

### -param ThreadInformationClass [in]

The class of information to retrieve. This value can be **ThreadMemoryPriority**, **ThreadAbsoluteCpuPriority** or **ThreadDynamicCodePolicy**.

> [!NOTE]
> **ThreadDynamicCodePolicy** is supported in Windows Server 2016 and newer, Windows 10 LTSB 2016 and newer, and Windows 10 version 1607 and newer.

### -param ThreadInformation

Pointer to a structure to receive the type of information specified by the *ThreadInformationClass* parameter.

If the *ThreadInformationClass* parameter is **ThreadMemoryPriority**, this parameter must point to a **MEMORY_PRIORITY_INFORMATION** structure.

If the *ThreadInformationClass* parameter is **ThreadAbsoluteCpuPriority**, this parameter must point to a **LONG**.

If the *ThreadInformationClass* parameter is **ThreadDynamicCodePolicy**, this parameter must point to a **DWORD**.

### -param ThreadInformationSize [in]

The size in bytes of the structure specified by the *ThreadInformation* parameter.

If the *ThreadInformationClass* parameter is **ThreadMemoryPriority**, this parameter must be `sizeof(MEMORY_PRIORITY_INFORMATION)`.  

If the *ThreadInformationClass* parameter is **ThreadAbsoluteCpuPriority**, this parameter must be `sizeof(LONG)`.

If the *ThreadInformationClass* parameter is **ThreadDynamicCodePolicy**, this parameter must be `sizeof(DWORD)`.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -see-also

[GetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessinformation), [SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)
