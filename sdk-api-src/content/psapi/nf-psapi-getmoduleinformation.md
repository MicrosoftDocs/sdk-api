---
UID: NF:psapi.GetModuleInformation
title: GetModuleInformation function (psapi.h)
description: Retrieves information about the specified module in the MODULEINFO structure.
helpviewer_keywords: ["GetModuleInformation","GetModuleInformation function [PSAPI]","K32GetModuleInformation","_win32_getmoduleinformation","base.getmoduleinformation","psapi.getmoduleinformation","psapi/GetModuleInformation","psapi/K32GetModuleInformation"]
old-location: psapi\getmoduleinformation.htm
tech.root: psapi
ms.assetid: afb9f4c8-c8ae-4497-96c1-b559cfa2cedf
ms.date: 12/05/2018
ms.keywords: GetModuleInformation, GetModuleInformation function [PSAPI], K32GetModuleInformation, _win32_getmoduleinformation, base.getmoduleinformation, psapi.getmoduleinformation, psapi/GetModuleInformation, psapi/K32GetModuleInformation
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetModuleInformation
 - psapi/GetModuleInformation
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
 - API-MS-Win-Core-PsAPI-Obsolete-L1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Core-PsAPI-L1-1-0.dll
api_name:
 - GetModuleInformation
 - K32GetModuleInformation
---

# GetModuleInformation function


## -description

Retrieves information about the specified module in the 
<a href="/windows/desktop/api/psapi/ns-psapi-moduleinfo">MODULEINFO</a> structure.

## -parameters

### -param hProcess [in]

A handle to the process that contains the module.

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param hModule [in]

A handle to the module.

### -param lpmodinfo [out]

A pointer to the 
<a href="/windows/desktop/api/psapi/ns-psapi-moduleinfo">MODULEINFO</a> structure that receives information about the module.

### -param cb [in]

The size of the 
<a href="/windows/desktop/api/psapi/ns-psapi-moduleinfo">MODULEINFO</a> structure, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To get information for the calling process, pass the handle returned by <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>.

The <b>GetModuleInformation</b> function does not retrieve information for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetModuleInformation</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as K32GetModuleInformation in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetModuleInformation</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    K32GetModuleInformation. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/api/psapi/ns-psapi-moduleinfo">MODULEINFO</a>



<a href="/windows/desktop/psapi/module-information">Module Information</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>