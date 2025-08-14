---
UID: NF:libloaderapi.GetModuleHandleA
title: GetModuleHandleA function (libloaderapi.h)
description: Retrieves a module handle for the specified module. The module must have been loaded by the calling process. (ANSI)
helpviewer_keywords: ["GetModuleHandleA", "libloaderapi/GetModuleHandleA"]
old-location: base\getmodulehandle.htm
tech.root: base
ms.assetid: 29514410-89fe-4888-8b34-0c30d5af237f
ms.date: 12/05/2018
ms.keywords: GetModuleHandle, GetModuleHandle function, GetModuleHandleA, GetModuleHandleW, _win32_getmodulehandle, base.getmodulehandle, libloaderapi/GetModuleHandle, libloaderapi/GetModuleHandleA, libloaderapi/GetModuleHandleW, winbase/GetModuleHandle, winbase/GetModuleHandleA, winbase/GetModuleHandleW
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetModuleHandleW (Unicode) and GetModuleHandleA (ANSI)
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
 - GetModuleHandleA
 - libloaderapi/GetModuleHandleA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
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
 - GetModuleHandle
 - GetModuleHandleA
 - GetModuleHandleW
---

# GetModuleHandleA function


## -description

Retrieves a module handle for the specified module. The module must have been loaded by the calling process.

To avoid the race conditions described in the Remarks section, use the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a> function.

## -parameters

### -param lpModuleName [in, optional]

The name of the loaded module (either a .dll or .exe file). If the file name extension is omitted, the default library extension .dll is appended. The file name string can include a trailing point character (.) to indicate that the module name has no extension. The string does not have to specify a path. When specifying a path, be sure to use backslashes (\\), not forward slashes (/). The name is compared (case independently) to the names of modules currently mapped into the address space of the calling process. 




If this parameter is NULL, 
<b>GetModuleHandle</b> returns a handle to the file used to create the calling process (.exe file).

The <b>GetModuleHandle</b> function does not retrieve handles for modules that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

## -returns

If the function succeeds, the return value is a handle to the specified module.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The returned handle is not global or inheritable. It cannot be duplicated or used by another process.

If <i>lpModuleName</i> does not include a path and there is more than one loaded module with the same base name and extension, you cannot predict which module handle will be returned. To work around this problem, you could specify a path, use <a href="/windows/desktop/Msi/side-by-side-assemblies">side-by-side assemblies</a>, or use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a> to specify a memory location rather than a DLL name. 

The 
<b>GetModuleHandle</b> function returns a handle to a mapped module without incrementing its reference count. However, if this handle is passed to the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> function, the reference count of the mapped module will be decremented. Therefore, do not pass a handle returned by <b>GetModuleHandle</b> to the 
<b>FreeLibrary</b> function. Doing so can cause a DLL module to be unmapped prematurely.

This function must be used carefully in a multithreaded application. There is no guarantee that the module handle remains valid between the time this function returns the handle and the time it is used. For example, suppose that a thread retrieves a module handle, but before it uses the handle, a second thread frees the module. If the system loads another module, it could reuse the module handle that was recently freed. Therefore, the first thread would have a handle to a different module  than the one intended.


#### Examples

For an example, see 
<a href="/windows/desktop/gdi/using-brushes">Using Brushes</a>.

<div class="code"></div>




> [!NOTE]
> The libloaderapi.h header defines GetModuleHandle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>
