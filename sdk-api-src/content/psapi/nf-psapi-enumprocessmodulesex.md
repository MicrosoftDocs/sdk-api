---
UID: NF:psapi.EnumProcessModulesEx
title: EnumProcessModulesEx function (psapi.h)
description: Retrieves a handle for each module in the specified process that meets the specified filter criteria.
helpviewer_keywords: ["EnumProcessModulesEx","EnumProcessModulesEx function [PSAPI]","K32EnumProcessModulesEx","LIST_MODULES_32BIT","LIST_MODULES_64BIT","LIST_MODULES_ALL","LIST_MODULES_DEFAULT","base.enumprocessmodulesex","psapi.enumprocessmodulesex","psapi/EnumProcessModulesEx","psapi/K32EnumProcessModulesEx"]
old-location: psapi\enumprocessmodulesex.htm
tech.root: psapi
ms.assetid: 0f982f32-31f4-47b6-85d2-d6e17aa4eeb9
ms.date: 12/05/2018
ms.keywords: EnumProcessModulesEx, EnumProcessModulesEx function [PSAPI], K32EnumProcessModulesEx, LIST_MODULES_32BIT, LIST_MODULES_64BIT, LIST_MODULES_ALL, LIST_MODULES_DEFAULT, base.enumprocessmodulesex, psapi.enumprocessmodulesex, psapi/EnumProcessModulesEx, psapi/K32EnumProcessModulesEx
req.header: psapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumProcessModulesEx
 - psapi/EnumProcessModulesEx
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
 - EnumProcessModulesEx
 - K32EnumProcessModulesEx
---

# EnumProcessModulesEx function


## -description

Retrieves a handle for each module in the specified process that meets the specified filter criteria.

## -parameters

### -param hProcess [in]

A handle to the process.

### -param lphModule [out]

An array that receives the list of module handles.

### -param cb [in]

The size of the <i>lphModule</i> array, in bytes.

### -param lpcbNeeded [out]

The number of bytes required to store all module handles in the <i>lphModule</i> array.

### -param dwFilterFlag [in]

The filter criteria. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LIST_MODULES_32BIT"></a><a id="list_modules_32bit"></a><dl>
<dt><b>LIST_MODULES_32BIT</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
List the 32-bit modules.

</td>
</tr>
<tr>
<td width="40%"><a id="LIST_MODULES_64BIT"></a><a id="list_modules_64bit"></a><dl>
<dt><b>LIST_MODULES_64BIT</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
List the 64-bit modules.

</td>
</tr>
<tr>
<td width="40%"><a id="LIST_MODULES_ALL"></a><a id="list_modules_all"></a><dl>
<dt><b>LIST_MODULES_ALL</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
List all modules.

</td>
</tr>
<tr>
<td width="40%"><a id="LIST_MODULES_DEFAULT"></a><a id="list_modules_default"></a><dl>
<dt><b>LIST_MODULES_DEFAULT</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Use the default behavior.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>EnumProcessModulesEx</b> function is primarily designed for use by debuggers and similar applications that must extract module information from another process. If the module list in the target process is corrupted or not yet initialized, or if the module list changes during the function call as a result of DLLs being loaded or unloaded, <b>EnumProcessModulesEx</b> may fail or return incorrect information.

This function is intended primarily for 64-bit applications. If the function is called by a 32-bit application running under WOW64, the <i>dwFilterFlag</i> option is ignored and the function provides the same results as the <a href="/windows/desktop/api/psapi/nf-psapi-enumprocessmodules">EnumProcessModules</a> function.

It is a good idea to specify a large array of <b>HMODULE</b> values, because it is hard to predict how many modules there will be in the process at the time you call 
<b>EnumProcessModulesEx</b>. To determine if the <i>lphModule</i> array is too small to hold all module handles for the process, compare the value returned in <i>lpcbNeeded</i> with the value specified in <i>cb</i>. If <i>lpcbNeeded</i> is greater than <i>cb</i>, increase the size of the array and call 
<b>EnumProcessModulesEx</b> again.

To determine how many modules were enumerated by the call to 
<b>EnumProcessModulesEx</b>, divide the resulting value in the <i>lpcbNeeded</i> parameter by <code>sizeof(HMODULE)</code>.

The <b>EnumProcessModulesEx</b> function does not retrieve handles for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

Do not call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> on any of the handles returned by this function. The information comes from a snapshot, so there are no resources to be freed.

To take a snapshot of specified processes and the heaps, modules, and threads used by these processes, use the <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load. 

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32EnumProcessModulesEx</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>EnumProcessModulesEx</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32EnumProcessModulesEx</b>. 

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>EnumProcessModulesEx</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/psapi/module-information">Module Information</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>