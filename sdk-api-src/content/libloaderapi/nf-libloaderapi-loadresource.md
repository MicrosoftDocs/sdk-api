---
UID: NF:libloaderapi.LoadResource
title: LoadResource function (libloaderapi.h)
description: Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.
helpviewer_keywords: ["LoadResource","LoadResource function [Menus and Other Resources]","_win32_LoadResource","_win32_loadresource_cpp","libloaderapi/LoadResource","menurc.loadresource","winui._win32_loadresource"]
old-location: menurc\loadresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\loadresource.htm
ms.date: 06/13/2025
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
 - LoadResource
---

# LoadResource function

## -description

Retrieves a handle that can be used to obtain a pointer to the first byte of the specified resource in memory.

## -parameters

### -param hModule [in, optional]

Type: **HMODULE**

A handle to the module whose executable file contains the resource. If *hModule* is **NULL**, the system loads the resource from the module that was used to create the current process.

### -param hResInfo [in]

Type: **HRSRC**

A handle to the resource to be loaded. This handle is returned by the <a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a> or <a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> function.

## -returns

Type: **HGLOBAL**

If the function succeeds, the return value is a handle to the data associated with the resource.

If the function fails, the return value is **NULL**. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The return type of **LoadResource** is **HGLOBAL** for backward compatibility, not because the function returns a handle to a global memory block. Do not pass this handle to the <a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> or <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function. To obtain a pointer to the first byte of the resource data, call the <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a> function; to obtain the size of the resource, call <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource">SizeofResource</a>.

[GlobalSize](/windows/desktop/api/winbase/nf-winbase-globalsize) returns 0 for a resource HGLOBAL. As a result, any APIs that depend on GlobalSize to determine the size of the HGLOBAL will not function correctly. For example, use [SHCreateMemStream](/windows/win32/api/shlwapi/nf-shlwapi-shcreatememstream) instead of [CreateStreamOnHGlobal](/windows/win32/api/combaseapi/nf-combaseapi-createstreamonhglobal).

To use a resource immediately, an application should use the following resource-specific functions to find and load the resource in one call.

| Function        | Action                                   | To remove resource         |
|-----------------|------------------------------------------|---------------------------|
| [FormatMessage](/windows/desktop/api/winbase/nf-winbase-formatmessage) | Loads and formats a message-table entry | No action needed           |
| [LoadAccelerators](/windows/win32/api/winuser/nf-winuser-loadacceleratorsa) | Loads an accelerator table               | [DestroyAcceleratorTable](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable) |
| [LoadBitmap](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) | Loads a bitmap resource                  | [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)         |
| [LoadCursor](/windows/win32/api/winuser/nf-winuser-loadcursora) | Loads a cursor resource                   | [DestroyCursor](/windows/win32/api/winuser/nf-winuser-destroycursor)       |
| [LoadIcon](/windows/win32/api/winuser/nf-winuser-loadicona)   | Loads an icon resource                    | [DestroyIcon](/windows/win32/api/winuser/nf-winuser-destroyicon)           |
| [LoadMenu](/windows/win32/api/winuser/nf-winuser-loadmenua)   | Loads a menu resource                     | [DestroyMenu](/windows/win32/api/winuser/nf-winuser-destroymenu)           |
| [LoadString](/windows/win32/api/winuser/nf-winuser-loadstringa) | Loads a string resource                  | No action needed           |

For example, an application can use the <a href="/windows/win32/api/winuser/nf-winuser-loadicona">LoadIcon</a> function to load an icon for display on the screen, followed by <a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> when done.

## Examples

For an example see <a href="/windows/win32/menurc/using-resources#updating-resources">Updating Resources</a>.

## -see-also

<a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a>

<a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>

<a href="/windows/desktop/api/winbase/nf-winbase-loadmodule">LoadModule</a>

<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a>
