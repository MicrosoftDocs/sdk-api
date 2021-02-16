---
UID: NF:psapi.QueryWorkingSetEx
title: QueryWorkingSetEx function (psapi.h)
description: Retrieves extended information about the pages at specific virtual addresses in the address space of the specified process.
helpviewer_keywords: ["K32QueryWorkingSetEx","QueryWorkingSetEx","QueryWorkingSetEx function [PSAPI]","base.queryworkingsetex","psapi.queryworkingsetex","psapi/K32QueryWorkingSetEx","psapi/QueryWorkingSetEx"]
old-location: psapi\queryworkingsetex.htm
tech.root: psapi
ms.assetid: 59ae76c9-e954-4648-9c9f-787136375b02
ms.date: 12/05/2018
ms.keywords: K32QueryWorkingSetEx, QueryWorkingSetEx, QueryWorkingSetEx function [PSAPI], base.queryworkingsetex, psapi.queryworkingsetex, psapi/K32QueryWorkingSetEx, psapi/QueryWorkingSetEx
req.header: psapi.h
req.include-header: 
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryWorkingSetEx
 - psapi/QueryWorkingSetEx
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
 - QueryWorkingSetEx
 - K32QueryWorkingSetEx
---

# QueryWorkingSetEx function


## -description

Retrieves extended information about the pages at specific virtual addresses in the address space of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param pv [in, out]

A pointer to an array of <a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_ex_information">PSAPI_WORKING_SET_EX_INFORMATION</a> structures. On input, each item in the array specifies a virtual address of interest. On output, each item in the array receives information about the corresponding virtual page.

### -param cb [in]

The size of the <i>pv</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Unlike the <a href="/windows/desktop/api/psapi/nf-psapi-queryworkingset">QueryWorkingSet</a> function, which is limited to the working set of the target process, the <b>QueryWorkingSetEx</b> function can be used to query addresses that are not in the process working set but are still part of the process, such as AWE and large pages.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as <b>K32QueryWorkingSetEx</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this function is defined as <b>QueryWorkingSetEx</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32QueryWorkingSetEx</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>QueryWorkingSetEx</b>. To ensure correct resolution of symbols, add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with "–DPSAPI_VERSION=1". To use run-time dynamic linking, load Psapi.dll.

#### Examples

For an example, see <a href="/windows/desktop/Memory/allocating-memory-from-a-numa-node">Allocating Memory from a NUMA Node</a>.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>

<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>

<a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_ex_information">PSAPI_WORKING_SET_EX_INFORMATION</a>

<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>