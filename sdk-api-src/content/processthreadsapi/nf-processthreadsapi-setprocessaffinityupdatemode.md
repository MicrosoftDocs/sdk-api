---
UID: NF:processthreadsapi.SetProcessAffinityUpdateMode
title: SetProcessAffinityUpdateMode function (processthreadsapi.h)
description: Sets the affinity update mode of the specified process.
helpviewer_keywords: ["PROCESS_AFFINITY_ENABLE_AUTO_UPDATE","SetProcessAffinityUpdateMode","SetProcessAffinityUpdateMode function","base.setprocessaffinityupdatemode","processthreadsapi/SetProcessAffinityUpdateMode","winbase/SetProcessAffinityUpdateMode"]
old-location: base\setprocessaffinityupdatemode.htm
tech.root: processthreadsapi
ms.assetid: 46e8f7d2-89b9-42cb-9171-d5ae2ec870da
ms.date: 12/05/2018
ms.keywords: PROCESS_AFFINITY_ENABLE_AUTO_UPDATE, SetProcessAffinityUpdateMode, SetProcessAffinityUpdateMode function, base.setprocessaffinityupdatemode, processthreadsapi/SetProcessAffinityUpdateMode, winbase/SetProcessAffinityUpdateMode
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SetProcessAffinityUpdateMode
 - processthreadsapi/SetProcessAffinityUpdateMode
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
 - SetProcessAffinityUpdateMode
---

# SetProcessAffinityUpdateMode function


## -description

Sets the affinity update mode of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must be returned by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> function.

### -param dwFlags [in]

The affinity update mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Disables dynamic update of the process affinity by the system.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_AFFINITY_ENABLE_AUTO_UPDATE"></a><a id="process_affinity_enable_auto_update"></a><dl>
<dt><b>PROCESS_AFFINITY_ENABLE_AUTO_UPDATE</b></dt>
<dt>0x00000001UL</dt>
</dl>
</td>
<td width="60%">
Enables dynamic update of the process affinity by the system.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system can adjust process affinity under various conditions, such as when a processor is added dynamically. By default, dynamic updates to the process affinity are disabled for each process. 

Processes should use this function to indicate whether they can handle dynamic adjustment of process affinity by the system. After a process enables affinity update mode, it can call this function to disable it. However, a process cannot enable affinity update mode after it has used this function to disable it.

Child processes do not inherit the affinity update mode of the parent process. The affinity update mode must be explicitly set for each child process.

To compile an application that calls this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode">QueryProcessAffinityUpdateMode</a>