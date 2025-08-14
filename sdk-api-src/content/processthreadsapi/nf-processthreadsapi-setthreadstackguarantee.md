---
UID: NF:processthreadsapi.SetThreadStackGuarantee
title: SetThreadStackGuarantee function (processthreadsapi.h)
description: Sets the minimum size of the stack associated with the calling thread or fiber that will be available during any stack overflow exceptions.
helpviewer_keywords: ["SetThreadStackGuarantee","SetThreadStackGuarantee function","base.setthreadstackguarantee","processthreadsapi/SetThreadStackGuarantee","winbase/SetThreadStackGuarantee"]
old-location: base\setthreadstackguarantee.htm
tech.root: processthreadsapi
ms.assetid: 42595cba-413b-4b71-8d32-f873ed78c39c
ms.date: 02/02/2024
ms.keywords: SetThreadStackGuarantee, SetThreadStackGuarantee function, base.setthreadstackguarantee, processthreadsapi/SetThreadStackGuarantee, winbase/SetThreadStackGuarantee
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - SetThreadStackGuarantee
 - processthreadsapi/SetThreadStackGuarantee
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - Vertdll.dll
api_name:
 - SetThreadStackGuarantee
---

# SetThreadStackGuarantee function

## -description

Sets the minimum size of the stack associated with the calling thread or fiber that will be available during any stack overflow exceptions. This is useful for handling stack overflow exceptions; the application can safely use the specified number of bytes during exception handling.

## -parameters

### -param StackSizeInBytes [in, out]

The size of the stack, in bytes. On return, this value is set to the size of the previous stack, in bytes.

If this parameter is 0 (zero), the function succeeds and the parameter contains the size of the current stack.

If the specified size is less than the current size, the function succeeds but ignores this request. Therefore, you cannot use this function to reduce the size of the stack.

This value cannot be larger than the reserved stack size.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the function is successful, the application can handle possible EXCEPTION_STACK_OVERFLOW exceptions using <a href="/windows/desktop/Debug/structured-exception-handling">structured exception handling</a>. To resume execution after handling a stack overflow, you must perform certain recovery steps. If you are using the Microsoft C/C++ compiler, call the <b>_resetstkoflw</b> function. If you are using another compiler, see the documentation for the compiler for information on recovering from stack overflows.

To set the stack guarantee for a fiber, you must first call the <a href="/windows/desktop/api/winbase/nf-winbase-switchtofiber">SwitchToFiber</a> function to execute the fiber. After you set the guarantee for this fiber, it is used by the fiber no matter which thread executes the fiber.

## -see-also

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Thread Stack Size](/windows/win32/ProcThread/thread-stack-size)

[Threads](/windows/win32/ProcThread/multiple-threads)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
