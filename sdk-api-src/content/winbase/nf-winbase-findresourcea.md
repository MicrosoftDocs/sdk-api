---
UID: NF:winbase.FindResourceA
title: FindResourceA function
author: windows-sdk-content
description: Determines the location of a resource with the specified type and name in the specified module.
old-location: menurc\findresource.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\findresource.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FindResource, FindResource function [Menus and Other Resources], FindResourceA, FindResourceW, _win32_FindResource, _win32_findresource_cpp, menurc.findresource, winbase/FindResource, winbase/FindResourceA, winbase/FindResourceW, winui._win32_findresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindResourceW (Unicode) and FindResourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
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
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - FindResource
 - FindResourceA
 - FindResourceW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindResourceA function


## -description


Determines the location of a resource with the specified type and name in the specified module.

To specify a language, use the <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> function.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose portable executable file or an accompanying MUI file contains the resource. If this parameter is <b>NULL</b>, the function searches the module used to create the current process.


### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.


### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given 

resource type. For standard resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. For more information, see the Remarks section below.


## -returns



Type: <b>HRSRC</b>

If the function succeeds, the return value is a handle to the specified resource's information block. To obtain a handle to the resource, pass this handle to the <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> function.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a> is <b>TRUE</b> for x = <i>lpName</i> or <i>lpType</i>, x specifies the integer identifier of the name or type of the given resource. Otherwise, those parameters are long pointers to null-terminated strings. If the first character of the string is a pound sign (#), the remaining characters represent a decimal number that specifies the integer identifier of the resource's name or type. For example, the string "#258" represents the integer identifier 258. 

To reduce the amount of memory required for a resource, an application should refer to it by integer identifier instead of by name. 

An application can use <b>FindResource</b> to find any type of resource, but this function should be used only if the application must access the binary resource data by making subsequent calls to <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> and then to <a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>. 

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
 

For example, an application can use the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function to load an icon for display on the screen. However, the application should use <b>FindResource</b> and <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> if it is loading the icon to copy its data to another application. 

String resources are stored in sections of up to 16 strings per section. The strings in each section are stored as a sequence of counted (not necessarily null-terminated) Unicode strings. The <a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a> function will extract the string resource from its corresponding section. 


#### Examples

For an example, see <a href="using_resources.htm">Updating Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>



<a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>



<a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>



<a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>



<a href="https://msdn.microsoft.com/e3eb82a3-15b6-4874-81d3-955d38d42383">SizeofResource</a>
 

 

