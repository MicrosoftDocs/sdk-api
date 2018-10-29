---
UID: NF:winbase.FindResourceExA
title: FindResourceExA function
author: windows-sdk-content
description: Determines the location of the resource with the specified type, name, and language in the specified module.
old-location: menurc\findresourceex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\findresourceex.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FindResourceEx, FindResourceEx function [Menus and Other Resources], FindResourceExA, FindResourceExW, _win32_FindResourceEx, _win32_findresourceex_cpp, menurc.findresourceex, winbase/FindResourceEx, winbase/FindResourceExA, winbase/FindResourceExW, winui._win32_findresourceex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindResourceExW (Unicode) and FindResourceExA (ANSI)
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
 - FindResourceEx
 - FindResourceExA
 - FindResourceExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindResourceExA function


## -description


Determines the location of the resource with the specified type, name, and language in the specified module.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose portable executable file or an accompanying MUI file contains the resource. If this parameter is <b>NULL</b>, the function searches the module used to create the current process.


### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given 

resource type. For standard resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. For more information, see the Remarks section below.


### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.


### -param wLanguage [in]

Type: <b>WORD</b>

The language of the resource. If this parameter is <code>MAKELANGID(LANG_NEUTRAL, SUBLANG_NEUTRAL)</code>, the current language associated with the calling thread is used.
        

To specify a language other than the current language, use the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro to create this parameter. For more information, see <b>MAKELANGID</b>.


## -returns



Type: <b>HRSRC</b>

If the function succeeds, the return value is a handle to the specified resource's information block. To obtain a handle to the resource, pass this handle to the <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> function.
                    

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a> is <b>TRUE</b> for x = <i>lpType</i> or <i>lpName</i>, x specifies the integer identifier of the type or name of the given resource. Otherwise, those parameters are long pointers to null-terminated strings. If the first character of the string is a pound sign (#), the remaining characters represent a decimal number that specifies the integer identifier of the resource's name or type. For example, the string "#258" represents the integer identifier 258. 

To reduce the amount of memory required for a resource, an application should refer to it by integer identifier instead of by name. 

An application can use <b>FindResourceEx</b> to find any type of resource, but this function should be used only if the application must access the binary resource data by making subsequent calls to <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> and then to <a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>. 

To use a resource immediately, an application should use one of the following resource-specific functions to find the resource and convert the data into a more usable form. 

<table class="clsStd">
<tr>
<th>Function</th>
<th>Action</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>
</td>
<td>Loads and formats a message-table entry.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>
</td>
<td>Loads an accelerator table.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>
</td>
<td>Loads a bitmap resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>
</td>
<td>Loads a cursor resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>
</td>
<td>Loads an icon resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>
</td>
<td>Loads a menu resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>
</td>
<td>Loads a string-table entry.</td>
</tr>
</table>
 

For example, an application can use the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function to load an icon for display on the screen. However, the application should use <b>FindResourceEx</b> and <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> if it is loading the icon to copy its data to another application. 

String resources are stored in sections of up to 16 strings per section. The strings in each section are stored as a sequence of counted (not necessarily null-terminated) Unicode strings. The <a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a> function will extract the string resource from its corresponding section. 


#### Examples

For an example, see <a href="using_resources.htm">Creating a Resource List</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>



<a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>



<a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

