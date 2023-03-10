---
UID: NF:psapi.EmptyWorkingSet
title: EmptyWorkingSet function (psapi.h)
description: Removes as many pages as possible from the working set of the specified process.
helpviewer_keywords: ["EmptyWorkingSet","EmptyWorkingSet function [PSAPI]","K32EmptyWorkingSet","_win32_emptyworkingset","base.emptyworkingset","psapi.emptyworkingset","psapi/EmptyWorkingSet","psapi/K32EmptyWorkingSet"]
old-location: psapi\emptyworkingset.htm
tech.root: psapi
ms.assetid: 76f2252e-7305-46b0-b1af-40ac084e6696
ms.date: 12/05/2018
ms.keywords: EmptyWorkingSet, EmptyWorkingSet function [PSAPI], K32EmptyWorkingSet, _win32_emptyworkingset, base.emptyworkingset, psapi.emptyworkingset, psapi/EmptyWorkingSet, psapi/K32EmptyWorkingSet
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
 - EmptyWorkingSet
 - psapi/EmptyWorkingSet
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
 - EmptyWorkingSet
 - K32EmptyWorkingSet
---

# EmptyWorkingSet function


## -description

Removes as many pages as possible from the working set of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right and the <b>PROCESS_SET_QUOTA</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can also empty the working set by calling  the <a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a> or <a href="/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex">SetProcessWorkingSetSizeEx</a> function with the <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> parameters set to the value <code>(SIZE_T)(-1)</code>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32EmptyWorkingSet</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as K32EmptyWorkingSet in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32EmptyWorkingSet</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    K32EmptyWorkingSet. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a>



<a href="/windows/desktop/Memory/working-set">Working Set</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>