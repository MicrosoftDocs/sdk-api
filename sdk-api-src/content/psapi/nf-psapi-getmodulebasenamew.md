---
UID: NF:psapi.GetModuleBaseNameW
title: GetModuleBaseNameW function (psapi.h)
description: Retrieves the base name of the specified module. (Unicode)
helpviewer_keywords: ["GetModuleBaseName", "GetModuleBaseName function [PSAPI]", "GetModuleBaseNameW", "K32GetModuleBaseName", "K32GetModuleBaseNameW", "_win32_getmodulebasename", "base.getmodulebasename", "psapi.getmodulebasename", "psapi/GetModuleBaseName", "psapi/GetModuleBaseNameW", "psapi/K32GetModuleBaseName", "psapi/K32GetModuleBaseNameW"]
old-location: psapi\getmodulebasename.htm
tech.root: psapi
ms.assetid: 31a9eb69-95f0-4dd7-8fd5-296f2cff0b8a
ms.date: 12/05/2018
ms.keywords: GetModuleBaseName, GetModuleBaseName function [PSAPI], GetModuleBaseNameA, GetModuleBaseNameW, K32GetModuleBaseName, K32GetModuleBaseNameA, K32GetModuleBaseNameW, _win32_getmodulebasename, base.getmodulebasename, psapi.getmodulebasename, psapi/GetModuleBaseName, psapi/GetModuleBaseNameA, psapi/GetModuleBaseNameW, psapi/K32GetModuleBaseName, psapi/K32GetModuleBaseNameA, psapi/K32GetModuleBaseNameW
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetModuleBaseNameW (Unicode) and GetModuleBaseNameA (ANSI)
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
 - GetModuleBaseNameW
 - psapi/GetModuleBaseNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-base-psapi-l1-1-0.dll
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-Obsolete-L1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Core-PsAPI-Ansi-L1-1-0.dll
 - API-Ms-Win-Core-PsAPI-L1-1-0.dll
api_name:
 - GetModuleBaseName
 - GetModuleBaseNameA
 - GetModuleBaseNameW
 - K32GetModuleBaseName
 - K32GetModuleBaseNameW
 - K32GetModuleBaseNameA
---

# GetModuleBaseNameW function


## -description

Retrieves the base name of the specified module.

## -parameters

### -param hProcess [in]

A handle to the process that contains the module. 

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param hModule [in, optional]

A handle to the module. If this parameter is NULL, this function  returns the name of the file used to create the calling process.

### -param lpBaseName [out]

A pointer to the buffer that receives the base name of the module. If the base name is longer than maximum number of characters specified by the <i>nSize</i> parameter, the base name is truncated.

### -param nSize [in]

The size of the <i>lpBaseName</i> buffer, in characters.

## -returns

If the function succeeds, the return value specifies the length of the string copied to the buffer, in characters.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetModuleBaseName</b> function is primarily designed for use by debuggers and similar applications that must extract module information from another process. If the module list in the target process is corrupted or is not yet initialized, or if the module list changes during the function call as a result of DLLs being loaded or unloaded, <b>GetModuleBaseName</b> may fail or return incorrect information.



To retrieve the base name of a module in the current process, use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamew">GetModuleFileName</a> function to retrieve the full module name and then use a function call such as <code>strrchr(szmodulename, '\\')</code> to scan to the beginning of the base name within the module name string. This is more efficient and more reliable than calling  <b>GetModuleBaseName</b>  with a handle to the current process.



To retrieve the base name of the main executable module for a remote process, use the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessimagefilenamew">GetProcessImageFileName</a> or <a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamew">QueryFullProcessImageName</a> function to retrieve the module name and then use the <code>strrchr</code> function as described in the previous paragraph. This is more efficient and more reliable than calling  <b>GetModuleBaseName</b>  with a NULL module handle.


The <b>GetModuleBaseName</b> function does not retrieve the base name for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexw">LoadLibraryEx</a>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetModuleBaseName</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetModuleBaseName</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetModuleBaseName</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetModuleBaseName</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
<a href="/windows/desktop/psapi/enumerating-all-processes">Enumerating All Processes</a>.

<div class="code"></div>




> [!NOTE]
> The psapi.h header defines GetModuleBaseName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexw">GetModuleFileNameEx</a>



<a href="/windows/desktop/psapi/module-information">Module Information</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/cpp/c-runtime-library/reference/strrchr-wcsrchr-mbsrchr-mbsrchr-l">strrchr, wcsrchr, _mbsrchr, _mbsrchr_l</a>
