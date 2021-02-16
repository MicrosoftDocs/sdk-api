---
UID: NF:psapi.GetWsChanges
title: GetWsChanges function (psapi.h)
description: Retrieves information about the pages that have been added to the working set of the specified process since the last time this function or the InitializeProcessForWsWatch function was called.
helpviewer_keywords: ["GetWsChanges","GetWsChanges function [PSAPI]","K32GetWsChanges","_win32_getwschanges","base.getwschanges","psapi.getwschanges","psapi.h/K32GetWsChanges","psapi/GetWsChanges","psapi/K32GetWsChanges"]
old-location: psapi\getwschanges.htm
tech.root: psapi
ms.assetid: ace5106c-9c7b-4d5f-a69a-c3a8bff0bb2d
ms.date: 12/05/2018
ms.keywords: GetWsChanges, GetWsChanges function [PSAPI], K32GetWsChanges, _win32_getwschanges, base.getwschanges, psapi.getwschanges, psapi.h/K32GetWsChanges, psapi/GetWsChanges, psapi/K32GetWsChanges
req.header: psapi.h
req.include-header: 
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetWsChanges
 - psapi/GetWsChanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - GetWsChanges
 - K32GetWsChanges
---

# GetWsChanges function


## -description

Retrieves information about the pages that have been added to the working set of the specified 
    process since the last time this function or the 
    <a href="/windows/desktop/api/psapi/nf-psapi-initializeprocessforwswatch">InitializeProcessForWsWatch</a> function was 
    called.

To retrieve extended information, use the 
    <a href="/windows/desktop/api/psapi/nf-psapi-getwschangesex">GetWsChangesEx</a> function.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> 
      access right. For more information, see 
      <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param lpWatchInfo [out]

A pointer to a user-allocated buffer that receives an array of 
      <a href="/windows/desktop/api/psapi/ns-psapi-psapi_ws_watch_information">PSAPI_WS_WATCH_INFORMATION</a> structures. 
      The array is terminated with a structure whose <b>FaultingPc</b> member is NULL.

### -param cb [in]

The size of the <i>lpWatchInfo</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_INSUFFICIENT_BUFFER</b> if the <i>lpWatchInfo</i> buffer is not 
       large enough to contain all the working set change records; the buffer is returned empty. Reallocate a larger 
       block of memory for the buffer and call again.

## -remarks

The operating system uses one buffer per process to maintain working set change records. If more than one 
    application (or multiple threads in the same application) calls this function with the same process handle, 
    neither application will have a complete accounting of the working set changes because each call empties the 
    buffer.

The operating system does not record new change records while it is processing the query (and emptying the 
    buffer). The function sets the error code to <b>NO_MORE_ENTRIES</b> if a concurrent query is 
    received while it is processing another query.

If the buffer becomes full, no new records are added to the buffer until this function or the 
    <a href="/windows/desktop/api/psapi/nf-psapi-initializeprocessforwswatch">InitializeProcessForWsWatch</a> function is 
    called. You should call this method with enough frequency to prevent possible data loss. If records are lost, the 
    array is terminated with a structure whose <b>FaultingPc</b> member is NULL and whose 
    <b>FaultingVa</b> member is set to the number of records that were lost.

<b>Windows Server 2003 and Windows XP:  </b>If records are lost, the array is terminated with a structure whose <b>FaultingPc</b> 
      member is NULL and whose <b>FaultingVa</b> member is 1.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetWsChanges</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetWsChanges</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetWsChanges</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetWsChanges</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/api/psapi/nf-psapi-initializeprocessforwswatch">InitializeProcessForWsWatch</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/windows/desktop/api/psapi/ns-psapi-psapi_ws_watch_information">PSAPI_WS_WATCH_INFORMATION</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>