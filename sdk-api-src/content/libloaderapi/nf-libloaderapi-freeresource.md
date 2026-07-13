---
UID: NF:libloaderapi.FreeResource
title: FreeResource function (libloaderapi.h)
description: Decrements (decreases by one) the reference count of a loaded resource. When the reference count reaches zero, the memory occupied by the resource is freed.
helpviewer_keywords: ["FreeResource","FreeResource function [Menus and Other Resources]","_win32_FreeResource","_win32_freeresource_cpp","libloaderapi/FreeResource","menurc.freeresource","winui._win32_freeresource"]
old-location: menurc\freeresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\freeresource.htm
ms.date: 12/05/2018
ms.keywords: FreeResource, FreeResource function [Menus and Other Resources], _win32_FreeResource, _win32_freeresource_cpp, libloaderapi/FreeResource, menurc.freeresource, winui._win32_freeresource
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
 - FreeResource
 - libloaderapi/FreeResource
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
 - FreeResource
---

## -description

> [!Note]
>This function is obsolete and is only supported for backward compatibility with 16-bit Windows. For 32-bit Windows applications, it is not necessary to free the resources loaded using <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>. For modern versions of Windows this function always returns <b>FALSE</b>.

Decrements (decreases by one) the reference count of a loaded resource. When the reference count reaches zero, the memory occupied by the resource is freed.

## -parameters

### -param hResData [in]

Type: <b>HGLOBAL</b>

A handle of the resource. It is assumed that <i>hglbResource</i> was created by <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is zero.

If the function fails, the return value is nonzero, which indicates that the resource has not been freed.

## -remarks

For resources loaded with other functions, <b>FreeResource</b> has been replaced by the following functions:

<table class="clsStd">
<tr>
<th>Resource type</th>
<th>FreeResource replacement</th>
</tr>
<tr>
<td>Accelerator</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>
</td>
</tr>
<tr>
<td>Bitmap</td>
<td>
<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
</td>
</tr>
<tr>
<td>Cursor</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>
</td>
</tr>
<tr>
<td>Icon</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>
</td>
</tr>
<tr>
<td>Menu</td>
<td>
<a href="/windows/win32/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>
</td>
</tr>
</table>
 

The reference count for a resource is incremented (increased by one) each time an application calls the <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> function for the resource.

The system automatically deletes these resources when the process that created them terminates. However, calling the appropriate function saves memory.  For more information, see <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/win32/api/winuser/nf-winuser-destroyacceleratortable">DestroyAcceleratorTable</a>



<a href="/windows/win32/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>



<a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/win32/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>



<b>Other Resources</b>



<b>Reference</b>
