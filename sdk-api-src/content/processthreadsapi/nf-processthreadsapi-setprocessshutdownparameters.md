---
UID: NF:processthreadsapi.SetProcessShutdownParameters
title: SetProcessShutdownParameters function (processthreadsapi.h)
description: Sets shutdown parameters for the currently calling process. This function sets a shutdown order for a process relative to the other processes in the system.
helpviewer_keywords: ["SHUTDOWN_NORETRY","SetProcessShutdownParameters","SetProcessShutdownParameters function","_win32_setprocessshutdownparameters","base.setprocessshutdownparameters","processthreadsapi/SetProcessShutdownParameters","winbase/SetProcessShutdownParameters"]
old-location: base\setprocessshutdownparameters.htm
tech.root: processthreadsapi
ms.assetid: c467950e-31e1-4608-a08a-0736a5524e0e
ms.date: 12/05/2018
ms.keywords: SHUTDOWN_NORETRY, SetProcessShutdownParameters, SetProcessShutdownParameters function, _win32_setprocessshutdownparameters, base.setprocessshutdownparameters, processthreadsapi/SetProcessShutdownParameters, winbase/SetProcessShutdownParameters
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - SetProcessShutdownParameters
 - processthreadsapi/SetProcessShutdownParameters
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
api_name:
 - SetProcessShutdownParameters
---

# SetProcessShutdownParameters function


## -description

Sets shutdown parameters for the currently calling process. This function sets a shutdown order for a process relative to the other processes in the system.

## -parameters

### -param dwLevel [in]

The shutdown priority for a process relative to other processes in the system. The system shuts down processes from high <i>dwLevel</i> values to low. The highest and lowest shutdown priorities are reserved for system components. This parameter must be in the following range of values. 



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

### -param dwFlags [in]

This parameter can be the following value.

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
The system terminates the process without displaying a retry dialog box for the user.

</td>
</tr>
</table>

## -returns

If the function is succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications running in the system security context do not get shut down by the operating system. They get notified of shutdown or logoff through the callback function installable via 
<a href="/windows/console/setconsolectrlhandler">SetConsoleCtrlHandler</a>. They also get notified in the order specified by the <i>dwLevel</i> parameter.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters">GetProcessShutdownParameters</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/console/setconsolectrlhandler">SetConsoleCtrlHandler</a>