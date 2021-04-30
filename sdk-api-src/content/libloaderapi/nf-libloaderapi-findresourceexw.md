---
UID: NF:libloaderapi.FindResourceExW
tech.root: menurc 
title: FindResourceExW
ms.date: 04/19/2021
targetos: Windows
description: Determines the location of the resource with the specified type, name, and language in the specified module.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: libloaderapi.h
req.idl: 
req.include-header: Windows.h 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only] 
req.target-min-winversvr: Windows 2000 Server [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Deprecated-APIs-Legacy-l1-1-0.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Deprecated-APIs-Legacy-l1-2-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - FindResourceExW
 - FindResourceEx
f1_keywords:
 - FindResourceExW
 - libloaderapi/FindResourceExW
 - FindResourceEx
 - libloaderapi/FindResourceEx
dev_langs:
 - c++
---

# FindResourceExW function

## -description

Determines the location of the resource with the specified type, name, and language in the specified module.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose portable executable file or an accompanying MUI file contains the resource. If this parameter is <b>NULL</b>, the function searches the module used to create the current process.

### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type. Alternately, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given resource type. For standard resource types, see <a href="/windows/desktop/menurc/resource-types">Resource Types</a>. For more information, see the Remarks section below.

### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource. Alternately, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.

### -param wLanguage [in]

Type: <b>WORD</b>

The language of the resource. If this parameter is <code>MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL)</code>, the current language associated with the calling thread is used.

To specify a language other than the current language, use the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro to create this parameter. For more information, see <b>MAKELANGID</b>.

## -returns

Type: <b>HRSRC</b>

If the function succeeds, the return value is a handle to the specified resource's information block. To obtain a handle to the resource, pass this handle to the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> function.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a> is <b>TRUE</b> for x = <i>lpType</i> or <i>lpName</i>, x specifies the integer identifier of the type or name of the given resource. Otherwise, those parameters are long pointers to null-terminated strings. If the first character of the string is a pound sign (#), the remaining characters represent a decimal number that specifies the integer identifier of the resource's name or type. For example, the string "#258" represents the integer identifier 258.

To reduce the amount of memory required for a resource, an application should refer to it by integer identifier instead of by name.

An application can use <b>FindResourceEx</b> to find any type of resource, but this function should be used only if the application must access the binary resource data by making subsequent calls to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> and then to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a>.

To use a resource immediately, an application should use one of the following resource-specific functions to find the resource and convert the data into a more usable form.

<table class="clsStd">
<tr>
<th>Function</th>
<th>Action</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>
</td>
<td>Loads and formats a message-table entry.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsw">LoadAccelerators</a>
</td>
<td>Loads an accelerator table.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapw">LoadBitmap</a>
</td>
<td>Loads a bitmap resource.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorw">LoadCursor</a>
</td>
<td>Loads a cursor resource.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadiconw">LoadIcon</a>
</td>
<td>Loads an icon resource.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuw">LoadMenu</a>
</td>
<td>Loads a menu resource.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-loadstringw">LoadString</a>
</td>
<td>Loads a string-table entry.</td>
</tr>
</table>

For example, an application can use the <a href="/windows/desktop/api/winuser/nf-winuser-loadiconw">LoadIcon</a> function to load an icon for display on the screen. However, the application should use <b>FindResourceEx</b> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> if it is loading the icon to copy its data to another application.

String resources are stored in sections of up to 16 strings per section. The strings in each section are stored as a sequence of counted (not necessarily null-terminated) Unicode strings. The <a href="/windows/desktop/api/winuser/nf-winuser-loadstringw">LoadString</a> function will extract the string resource from its corresponding section.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-findresourcew.md">FindResource</a>  
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsw">LoadAccelerators</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapw">LoadBitmap</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorw">LoadCursor</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadiconw">LoadIcon</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuw">LoadMenu</a>  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>  
<a href="/windows/desktop/api/winuser/nf-winuser-loadstringw">LoadString</a>  
<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>  

<b>Other Resources</b>

<b>Reference</b>  
<a href="/windows/desktop/menurc/resources">Resources</a>  
