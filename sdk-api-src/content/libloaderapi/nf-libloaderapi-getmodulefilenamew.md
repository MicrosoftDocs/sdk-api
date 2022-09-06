---
UID: NF:libloaderapi.GetModuleFileNameW
title: GetModuleFileNameW function (libloaderapi.h)
description: Retrieves the fully qualified path for the file that contains the specified module. The module must have been loaded by the current process.
helpviewer_keywords: ["GetModuleFileName","GetModuleFileName function","GetModuleFileNameA","GetModuleFileNameW","_win32_getmodulefilename","base.getmodulefilename","libloaderapi/GetModuleFileName","libloaderapi/GetModuleFileNameA","libloaderapi/GetModuleFileNameW","winbase/GetModuleFileName","winbase/GetModuleFileNameA","winbase/GetModuleFileNameW"]
old-location: base\getmodulefilename.htm
tech.root: base
ms.assetid: f124c99f-8be1-4a9c-a84c-b1b323921f1a
ms.date: 12/05/2018
ms.keywords: GetModuleFileName, GetModuleFileName function, GetModuleFileNameA, GetModuleFileNameW, _win32_getmodulefilename, base.getmodulefilename, libloaderapi/GetModuleFileName, libloaderapi/GetModuleFileNameA, libloaderapi/GetModuleFileNameW, winbase/GetModuleFileName, winbase/GetModuleFileNameA, winbase/GetModuleFileNameW
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetModuleFileNameW (Unicode) and GetModuleFileNameA (ANSI)
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
 - GetModuleFileNameW
 - libloaderapi/GetModuleFileNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - GetModuleFileName
 - GetModuleFileNameA
 - GetModuleFileNameW
---

# GetModuleFileNameW function


## -description

Retrieves the fully qualified path for the file that contains the specified module. The module must have been loaded by the current process.

To locate the file for a module that was loaded by another process, use the 
<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a> function.

## -parameters

### -param hModule [in, optional]

A handle to the loaded module whose path is being requested. If this parameter is <b>NULL</b>, 
<b>GetModuleFileName</b> retrieves the path of the executable file of the current process.

The <b>GetModuleFileName</b> function does not retrieve the path for modules  that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

### -param lpFilename [out]

A pointer to a buffer that receives the fully qualified path of the module. If the length of the path is less than the size that the <i>nSize</i> parameter specifies, the function succeeds and the path is returned as a null-terminated string. 

If the length of the path exceeds the size that  the <i>nSize</i> parameter specifies, the function succeeds and the string is truncated to <i>nSize</i>  characters including the terminating null character.

<b>Windows XP:  </b>The string is truncated to <i>nSize</i> characters and is not null-terminated.

The string returned will use the same format that was specified when the module was loaded. Therefore, the path can be a long or short file name, and can use the prefix "\\?\". For more information, see 
<a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

### -param nSize [in]

The size of the <i>lpFilename</i> buffer, in <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is the length of the string that is copied to the buffer, in characters, not including the terminating null character. If the buffer is too small to hold the module name, the string is truncated to <i>nSize</i> characters including the terminating null character, the function returns <i>nSize</i>, and the function sets the last error to <b>ERROR_INSUFFICIENT_BUFFER</b>.

<b>Windows XP:  </b>If the buffer is too small to hold the module name, the function returns <i>nSize</i> and the last error code is not modified. If <i>nSize</i> is zero, the return value is zero and the last error code is not modified.

If the function fails, the return value is 0 (zero). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a DLL is loaded in two processes, its file name in one process may differ in case from its file name in the other process.

The global variable <code>_pgmptr</code> is automatically initialized to the full path of the executable file, and can be used to retrieve the full path name of an executable file. 


#### Examples

For an example, see 
<a href="/windows/desktop/Services/installing-a-service">Installing a Service</a>.

<div class="code"></div>




> [!NOTE]
> The libloaderapi.h header defines GetModuleFileName as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>
