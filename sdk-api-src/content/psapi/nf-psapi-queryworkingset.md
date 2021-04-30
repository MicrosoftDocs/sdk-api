---
UID: NF:psapi.QueryWorkingSet
title: QueryWorkingSet function (psapi.h)
description: Retrieves information about the pages currently added to the working set of the specified process.
helpviewer_keywords: ["K32QueryWorkingSet","QueryWorkingSet","QueryWorkingSet function [PSAPI]","_win32_queryworkingset","base.queryworkingset","psapi.queryworkingset","psapi/K32QueryWorkingSet","psapi/QueryWorkingSet"]
old-location: psapi\queryworkingset.htm
tech.root: psapi
ms.assetid: b932153f-2bbd-460e-8ff7-b3e493c397bb
ms.date: 12/05/2018
ms.keywords: K32QueryWorkingSet, QueryWorkingSet, QueryWorkingSet function [PSAPI], _win32_queryworkingset, base.queryworkingset, psapi.queryworkingset, psapi/K32QueryWorkingSet, psapi/QueryWorkingSet
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
 - QueryWorkingSet
 - psapi/QueryWorkingSet
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
 - QueryWorkingSet
 - K32QueryWorkingSet
---

# QueryWorkingSet function


## -description

Retrieves information about the pages currently added to the working set of the specified 
    process.

To retrieve working set information for a subset of virtual addresses, or to retrieve information about pages 
    that are not part of the working set (such as AWE or large pages), use the 
    <a href="/windows/desktop/api/psapi/nf-psapi-queryworkingsetex">QueryWorkingSetEx</a> function.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and 
      <b>PROCESS_VM_READ</b> access rights. For more information, see 
      <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param pv [out]

A pointer to the buffer that receives the information. For more information, see 
       <a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_information">PSAPI_WORKING_SET_INFORMATION</a>.

If the buffer pointed to by the <i>pv</i> parameter is not large enough to contain all 
       working set entries for the target process, the function fails with <b>ERROR_BAD_LENGTH</b>. 
       In this case, the <b>NumberOfEntries</b> member of the 
       <a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_information">PSAPI_WORKING_SET_INFORMATION</a> 
       structure is set to the required number of entries, but the function does not return information about the 
       working set entries.

### -param cb [in]

The size of the <i>pv</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32QueryWorkingSet</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>QueryWorkingSet</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32QueryWorkingSet</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as <b>QueryWorkingSet</b>. 
    To ensure correct resolution of symbols, add Psapi.lib to the 
    <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load 
    Psapi.dll.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_information">PSAPI_WORKING_SET_INFORMATION</a>



<a href="/windows/desktop/api/psapi/nf-psapi-queryworkingsetex">QueryWorkingSetEx</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>