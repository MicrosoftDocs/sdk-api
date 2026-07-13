---
UID: NF:psapi.GetProcessImageFileNameA
title: GetProcessImageFileNameA function (psapi.h)
description: Retrieves the name of the executable file for the specified process. (ANSI)
helpviewer_keywords: ["GetProcessImageFileNameA", "K32GetProcessImageNameA", "K32GetProcessImageNameW", "psapi/GetProcessImageFileNameA", "psapi/K32GetProcessImageNameA", "psapi/K32GetProcessImageNameW"]
old-location: psapi\getprocessimagefilename.htm
tech.root: psapi
ms.assetid: 819fc2f4-0801-417b-9cbb-d7fd2894634e
ms.date: 12/05/2018
ms.keywords: GetProcessImageFileName, GetProcessImageFileName function [PSAPI], GetProcessImageFileNameA, GetProcessImageFileNameW, K32GetProcessImageFileName, K32GetProcessImageNameA, K32GetProcessImageNameW, _win32_getprocessimagefilename, base.getprocessimagefilename, psapi.getprocessimagefilename, psapi/GetProcessImageFileName, psapi/GetProcessImageFileNameA, psapi/GetProcessImageFileNameW, psapi/K32GetProcessImageFileName, psapi/K32GetProcessImageNameA, psapi/K32GetProcessImageNameW
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetProcessImageFileNameW (Unicode) and GetProcessImageFileNameA (ANSI)
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
 - GetProcessImageFileNameA
 - psapi/GetProcessImageFileNameA
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
api_name:
 - GetProcessImageFileName
 - GetProcessImageFileNameA
 - GetProcessImageFileNameW
 - K32GetProcessImageFileName
 - K32GetProcessImageNameW
 - K32GetProcessImageNameA
---

# GetProcessImageFileNameA function


## -description

Retrieves the name of the executable file for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b>  or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

### -param lpImageFileName [out]

A pointer to a buffer that receives the full path to the executable file.

### -param nSize [in]

The size of the <i>lpImageFileName</i> buffer, in characters.

## -returns

If the function succeeds, the return value specifies the length of the string copied to the buffer.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The file Psapi.dll is installed in the %windir%\System32 directory. If there is another copy of this DLL on your computer, it can lead to the following error when running applications on your system: "The procedure entry point GetProcessImageFileName could not be located in the dynamic link library PSAPI.DLL." To work around this problem, locate any versions that are not in the %windir%\System32 directory and delete or rename them, then restart.

The <b>GetProcessImageFileName</b> function returns the path in device form, rather than drive letters. For example, the file name C:\Windows\System32\Ctype.nls would look as follows in device form:



\Device\Harddisk0\Partition1\Windows\System32\Ctype.nls

To retrieve the module name of the current process, use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a> function with a NULL module handle. This is more efficient than calling the <b>GetProcessImageFileName</b> function with a handle to the current process.

To retrieve the name of the main executable module for a remote process in win32 path format, use the <a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a> function.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetProcessImageFileName</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetProcessImageFileName</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetProcessImageFileName</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetProcessImageFileName</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.





> [!NOTE]
> The psapi.h header defines GetProcessImageFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>



<a href="/windows/desktop/psapi/process-information">Process Information</a>



<a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a>
