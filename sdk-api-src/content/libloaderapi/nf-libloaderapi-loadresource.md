---
UID: NF:libloaderapi.LoadResource
title: LoadResource function (libloaderapi.h)
description: Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.
helpviewer_keywords: ["LoadResource","LoadResource function [Menus and Other Resources]","_win32_LoadResource","_win32_loadresource_cpp","libloaderapi/LoadResource","menurc.loadresource","winui._win32_loadresource"]
old-location: menurc\loadresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\loadresource.htm
ms.date: 12/05/2018
ms.keywords: LoadResource, LoadResource function [Menus and Other Resources], _win32_LoadResource, _win32_loadresource_cpp, libloaderapi/LoadResource, menurc.loadresource, winui._win32_loadresource
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - LoadResource
 - libloaderapi/LoadResource
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
 - LoadResource
---

# LoadResource function


## -description

Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resource. If <i>hModule</i> is <b>NULL</b>, the system loads the resource from the module that was used to create the current process.

### -param hResInfo [in]

Type: <b>HRSRC</b>

A handle to the resource to be loaded. This handle is returned by the <a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a> or <a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> function.

## -returns

Type: <b>HGLOBAL</b>

If the function succeeds, the return value is a handle to the data associated with the resource.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The return type of <b>LoadResource</b> is <b>HGLOBAL</b> for backward compatibility, not because the function returns a handle to a global memory block. Do not pass this handle to the <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> or <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function. To obtain a pointer to the first byte of the resource data, call the <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a> function; to obtain the size of the resource, call <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource">SizeofResource</a>. 

Note that [GlobalSize](/windows/desktop/api/winbase/nf-winbase-globalsize) will return 0 for a resource HGLOBAL. As a result, any APIs that depend on GlobalSize to determine the size of the HGLOBAL will not function correctly.
For example, don't use [CreateStreamOnHGlobal](/windows/win32/api/combaseapi/nf-combaseapi-createstreamonhglobal), as it relies on it. Instead, use [SHCreateMemStream](/windows/win32/api/shlwapi/nf-shlwapi-shcreatememstream).

To use a resource immediately, an application should use the following resource-specific functions to find and load the resource in one call.

<table class="clsStd">
<tr>
<th>Function</th>
<th>Action</th>
<th>To remove resource</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>
</td>
<td>Loads and formats a message-table entry</td>
<td>No action needed</td>
</tr>
<tr>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>
</td>
<td>Loads an accelerator table</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>
</td>
<td>Loads a bitmap resource</td>
<td>
<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-loadcursora">LoadCursor</a>
</td>
<td>Loads a cursor resource</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-loadicona">LoadIcon</a>
</td>
<td>Loads an icon resource</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-loadmenua">LoadMenu</a>
</td>
<td>Loads a menu resource</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-loadstringa">LoadString</a>
</td>
<td>Loads a string resource</td>
<td>No action needed</td>
</tr>
</table>
 

For example, an application can use the <a href="/windows/win32/api/winuser/nf-winuser-loadicona">LoadIcon</a> function to load an icon for display on the screen, followed by <a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> when done. 


#### Examples

For an example see <a href="/windows/win32/menurc/using-resources#updating-resources">Updating Resources</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/winbase/nf-winbase-loadmodule">LoadModule</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
