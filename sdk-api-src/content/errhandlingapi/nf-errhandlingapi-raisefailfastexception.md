---
UID: NF:errhandlingapi.RaiseFailFastException
title: RaiseFailFastException function (errhandlingapi.h)
description: Raises an exception that bypasses all exception handlers (frame or vector based).
helpviewer_keywords: ["FAIL_FAST_GENERATE_EXCEPTION_ADDRESS","RaiseFailFastException","RaiseFailFastException function","base.raisefailfastexception","errhandlingapi/RaiseFailFastException"]
old-location: base\raisefailfastexception.htm
tech.root: Debug
ms.assetid: 69fbb722-2733-4035-8bfa-a5828311581c
ms.date: 12/05/2018
ms.keywords: FAIL_FAST_GENERATE_EXCEPTION_ADDRESS, RaiseFailFastException, RaiseFailFastException function, base.raisefailfastexception, errhandlingapi/RaiseFailFastException
req.header: errhandlingapi.h
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
 - RaiseFailFastException
 - errhandlingapi/RaiseFailFastException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - RaiseFailFastException
---

# RaiseFailFastException function


## -description

Raises an exception that bypasses all exception handlers (frame or vector based). Raising this exception terminates the application and invokes Windows Error Reporting, if Windows Error Reporting is enabled.

## -parameters

### -param pExceptionRecord [in, optional]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> structure that contains the exception information. You must specify the <b>ExceptionAddress</b> and <b>ExceptionCode</b> members.

If this parameter is <b>NULL</b>, the function creates an exception record and sets the <b>ExceptionCode</b> member to STATUS_FAIL_FAST_EXCEPTION. The function will also set the <b>ExceptionAddress</b> member if the <i>dwFlags</i> parameter contains the FAIL_FAST_GENERATE_EXCEPTION_ADDRESS flag.

### -param pContextRecord [in, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that contains the context information. If <b>NULL</b>, this function generates the context (however, the context will not exactly match the context of the caller).

### -param dwFlags [in]

You can specify zero or the following flag that control this function's behavior:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FAIL_FAST_GENERATE_EXCEPTION_ADDRESS"></a><a id="fail_fast_generate_exception_address"></a><dl>
<dt><b>FAIL_FAST_GENERATE_EXCEPTION_ADDRESS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Causes <b>RaiseFailFastException</b> to set the <b>ExceptionAddress</b> of <a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> to the return address of this function (the next instruction in the caller after the call to <b>RaiseFailFastException</b>). This function will set the exception address only if <b>ExceptionAddress</b> is not <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Typically, you call this function if your application is in a bad state and you want to terminate the application  immediately and have a Windows Error Report created.

If the WER service is disabled or cannot be started or there is no debugger attached to the process, the process will be terminated.

This function raises a second chance exception. If JIT debugging is enabled, a debugger will attach to the process.

## -see-also

<b>Environment.FailFast</b>