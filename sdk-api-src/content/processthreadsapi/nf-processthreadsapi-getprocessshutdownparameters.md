---
UID: NF:processthreadsapi.GetProcessShutdownParameters
title: GetProcessShutdownParameters function (processthreadsapi.h)
description: Retrieves the shutdown parameters for the currently calling process.
helpviewer_keywords: ["GetProcessShutdownParameters","GetProcessShutdownParameters function","SHUTDOWN_NORETRY","_win32_getprocessshutdownparameters","base.getprocessshutdownparameters","processthreadsapi/GetProcessShutdownParameters"]
old-location: base\getprocessshutdownparameters.htm
tech.root: processthreadsapi
ms.assetid: 68b48e67-c7e0-4434-bef5-b2aaebb343ff
ms.date: 12/05/2018
ms.keywords: GetProcessShutdownParameters, GetProcessShutdownParameters function, SHUTDOWN_NORETRY, _win32_getprocessshutdownparameters, base.getprocessshutdownparameters, processthreadsapi/GetProcessShutdownParameters
req.header: processthreadsapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessShutdownParameters
 - processthreadsapi/GetProcessShutdownParameters
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
 - API-Ms-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
api_name:
 - GetProcessShutdownParameters
---

# GetProcessShutdownParameters function


## -description

Retrieves the shutdown parameters for the currently calling process.

## -parameters

### -param lpdwLevel [out]

A pointer to a variable that receives the shutdown priority level. Higher levels shut down first. System level shutdown orders are reserved for system components. Higher numbers shut down first. Following are the level conventions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>000-0FF</dt>
</dl>
</td>
<td width="60%">
System reserved last shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>100-1FF</dt>
</dl>
</td>
<td width="60%">
Application reserved last shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>200-2FF</dt>
</dl>
</td>
<td width="60%">
Application reserved "in between" shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>300-3FF</dt>
</dl>
</td>
<td width="60%">
Application reserved first shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>400-4FF</dt>
</dl>
</td>
<td width="60%">
System reserved first shutdown range.

</td>
</tr>
</table>
 

All processes start at shutdown level 0x280.

### -param lpdwFlags [out]

A pointer to a variable that receives the shutdown flags. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_NORETRY"></a><a id="shutdown_noretry"></a><dl>
<dt><b>SHUTDOWN_NORETRY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this process takes longer than the specified timeout to shut down, do not display a retry dialog box for the user. Instead, just cause the process to directly exit.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters">SetProcessShutdownParameters</a>