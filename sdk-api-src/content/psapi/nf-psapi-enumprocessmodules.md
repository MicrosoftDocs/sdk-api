---
UID: NF:psapi.EnumProcessModules
title: EnumProcessModules function (psapi.h)
description: Retrieves a handle for each module in the specified process.
helpviewer_keywords: ["EnumProcessModules","EnumProcessModules function [PSAPI]","K32EnumProcessModules","_win32_enumprocessmodules","base.enumprocessmodules","psapi.enumprocessmodules","psapi/EnumProcessModules","psapi/K32EnumProcessModules"]
old-location: psapi\enumprocessmodules.htm
tech.root: psapi
ms.assetid: b4088506-2f69-4cf0-9bab-3e6a7185f5b2
ms.date: 12/05/2018
ms.keywords: EnumProcessModules, EnumProcessModules function [PSAPI], K32EnumProcessModules, _win32_enumprocessmodules, base.enumprocessmodules, psapi.enumprocessmodules, psapi/EnumProcessModules, psapi/K32EnumProcessModules
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
 - EnumProcessModules
 - psapi/EnumProcessModules
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
 - EnumProcessModules
 - K32EnumProcessModules
---

# EnumProcessModules function


## -description

Retrieves a handle for each module in the specified process.

To control whether a 64-bit application enumerates 32-bit modules, 64-bit modules, or both types of modules, use 
    the <a href="/windows/desktop/api/psapi/nf-psapi-enumprocessmodulesex">EnumProcessModulesEx</a> function.

## -parameters

### -param hProcess [in]

 A handle to the process.

### -param lphModule [out]

An array that receives the list of module handles.

### -param cb [in]

The size of the <i>lphModule</i> array, in bytes.

### -param lpcbNeeded [out]

The number of bytes required to store all module handles in the <i>lphModule</i> 
      array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>EnumProcessModules</b> function is primarily 
    designed for use by debuggers and similar applications that must extract module information from another process. 
    If the module list in the target process is corrupted or not yet initialized, or if the module list changes during 
    the function call as a result of DLLs being loaded or unloaded, 
    <b>EnumProcessModules</b> may fail or return incorrect 
    information.

It is a good idea to specify a large array of <b>HMODULE</b> values, because it is hard 
    to predict how many modules there will be in the process at the time you call 
    <b>EnumProcessModules</b>. To determine if the 
    <i>lphModule</i> array is too small to hold all module handles for the process, compare the 
    value returned in <i>lpcbNeeded</i> with the value specified in <i>cb</i>. 
    If <i>lpcbNeeded</i> is greater than <i>cb</i>, increase the size of the 
    array and call <b>EnumProcessModules</b> again.

To determine how many modules were enumerated by the call to 
    <b>EnumProcessModules</b>, divide the resulting value in 
    the <i>lpcbNeeded</i> parameter by 
    <code>sizeof(HMODULE)</code>.

The <b>EnumProcessModules</b> function does not 
    retrieve handles for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> or similar  flags. 
    For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

Do not call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> on any of the handles returned 
    by this function. The information comes from a snapshot, so there are no resources to be freed.

If this function is called from a 32-bit application running on WOW64, it can only enumerate the modules of a 
    32-bit process. If the process is a 64-bit process, this function fails and the last error code is 
    <b>ERROR_PARTIAL_COPY</b> (299).

To take a snapshot of specified processes and the heaps, modules, and threads used by these processes, use the 
    <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32EnumProcessModules</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>EnumProcessModules</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32EnumProcessModules</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as 
    <b>EnumProcessModules</b>. To ensure correct resolution 
    of symbols, add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the 
    program with <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load 
    Psapi.dll.


#### Examples

For an example, see 
     <a href="/windows/desktop/psapi/enumerating-all-processes">Enumerating All Processes</a> or 
     <a href="/windows/desktop/psapi/enumerating-all-modules-for-a-process">Enumerating All Modules for a Process</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/psapi/nf-psapi-enumprocessmodulesex">EnumProcessModulesEx</a>



<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/psapi/module-information">Module Information</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>