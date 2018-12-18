---
UID: NF:libloaderapi.GetModuleHandleW
title: GetModuleHandleW function
author: windows-sdk-content
description: Retrieves a module handle for the specified module. The module must have been loaded by the calling process.
old-location: base\getmodulehandle.htm
tech.root: Dlls
ms.assetid: 29514410-89fe-4888-8b34-0c30d5af237f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetModuleHandle, GetModuleHandle function, GetModuleHandleA, GetModuleHandleW, _win32_getmodulehandle, base.getmodulehandle, libloaderapi/GetModuleHandle, libloaderapi/GetModuleHandleA, libloaderapi/GetModuleHandleW, winbase/GetModuleHandle, winbase/GetModuleHandleA, winbase/GetModuleHandleW
ms.topic: function
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
 - GetModuleHandle
 - GetModuleHandleA
 - GetModuleHandleW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetModuleHandleW function


## -description


Retrieves a module handle for the specified module. The module must have been loaded by the calling process.

To avoid the race conditions described in the Remarks section, use the 
<a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a> function.


## -parameters




### -param lpModuleName [in, optional]

The name of the loaded module (either a .dll or .exe file). If the file name extension is omitted, the default library extension .dll is appended. The file name string can include a trailing point character (.) to indicate that the module name has no extension. The string does not have to specify a path. When specifying a path, be sure to use backslashes (\), not forward slashes (/). The name is compared (case independently) to the names of modules currently mapped into the address space of the calling process. 




If this parameter is NULL, 
<b>GetModuleHandle</b> returns a handle to the file used to create the calling process (.exe file).

The <b>GetModuleHandle</b> function does not retrieve handles for modules that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>.


## -returns



If the function succeeds, the return value is a handle to the specified module.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The returned handle is not global or inheritable. It cannot be duplicated or used by another process.

If <i>lpModuleName</i> does not include a path and there is more than one loaded module with the same base name and extension, you cannot predict which module handle will be returned. To work around this problem, you could specify a path, use <a href="https://msdn.microsoft.com/en-us/library/Aa371852(v=VS.85).aspx">side-by-side assemblies</a>, or use <a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a> to specify a memory location rather than a DLL name. 

The 
<b>GetModuleHandle</b> function returns a handle to a mapped module without incrementing its reference count. However, if this handle is passed to the <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> function, the reference count of the mapped module will be decremented. Therefore, do not pass a handle returned by <b>GetModuleHandle</b> to the 
<b>FreeLibrary</b> function. Doing so can cause a DLL module to be unmapped prematurely.

This function must be used carefully in a multithreaded application. There is no guarantee that the module handle remains valid between the time this function returns the handle and the time it is used. For example, suppose that a thread retrieves a module handle, but before it uses the handle, a second thread frees the module. If the system loads another module, it could reuse the module handle that was recently freed. Therefore, the first thread would have a handle to a different module  than the one intended.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/64cd6e82-7a0d-4b5e-b491-450f37eea43a">Using Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>



<a href="https://msdn.microsoft.com/f124c99f-8be1-4a9c-a84c-b1b323921f1a">GetModuleFileName</a>



<a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>
 

 

