---
UID: NF:winbase.FindResourceA
title: FindResourceA function
author: windows-sdk-content
description: Determines the location of a resource with the specified type and name in the specified module.
old-location: menurc\findresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\findresource.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FindResource, FindResource function [Menus and Other Resources], FindResourceA, FindResourceW, _win32_FindResource, _win32_findresource_cpp, menurc.findresource, winbase/FindResource, winbase/FindResourceA, winbase/FindResourceW, winui._win32_findresource
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
req.unicode-ansi: FindResourceW (Unicode) and FindResourceA (ANSI)
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
req.typenames: 
req.redist: 
---

# FindResourceA function


## -description


Determines the location of a resource with the specified type and name in the specified module.

To specify a language, use the <a href="https://msdn.microsoft.com/en-us/library/ms648043(v=VS.85).aspx">FindResourceEx</a> function.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose portable executable file or an accompanying MUI file contains the resource. If this parameter is <b>NULL</b>, the function searches the module used to create the current process.


### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.


### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given 

resource type. For standard resource types, see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Resource Types</a>. For more information, see the Remarks section below.


## -returns



Type: <b>HRSRC</b>

If the function succeeds, the return value is a handle to the specified resource's information block. To obtain a handle to the resource, pass this handle to the <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a> function.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/en-us/library/ms648028(v=VS.85).aspx">IS_INTRESOURCE</a> is <b>TRUE</b> for x = <i>lpName</i> or <i>lpType</i>, x specifies the integer identifier of the name or type of the given resource. Otherwise, those parameters are long pointers to null-terminated strings. If the first character of the string is a pound sign (#), the remaining characters represent a decimal number that specifies the integer identifier of the resource's name or type. For example, the string "#258" represents the integer identifier 258. 

To reduce the amount of memory required for a resource, an application should refer to it by integer identifier instead of by name. 

An application can use <b>FindResource</b> to find any type of resource, but this function should be used only if the application must access the binary resource data by making subsequent calls to <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a> and then to <a href="https://msdn.microsoft.com/en-us/library/ms648047(v=VS.85).aspx">LockResource</a>. 

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
<a href="https://msdn.microsoft.com/en-us/library/ms646370(v=VS.85).aspx">LoadAccelerators</a>
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
<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>
</td>
<td>Loads a cursor resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>
</td>
<td>Loads an icon resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms647990(v=VS.85).aspx">LoadMenu</a>
</td>
<td>Loads a menu resource.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms647486(v=VS.85).aspx">LoadString</a>
</td>
<td>Loads a string-table entry.</td>
</tr>
</table>
 

For example, an application can use the <a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a> function to load an icon for display on the screen. However, the application should use <b>FindResource</b> and <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a> if it is loading the icon to copy its data to another application. 

String resources are stored in sections of up to 16 strings per section. The strings in each section are stored as a sequence of counted (not necessarily null-terminated) Unicode strings. The <a href="https://msdn.microsoft.com/en-us/library/ms647486(v=VS.85).aspx">LoadString</a> function will extract the string resource from its corresponding section. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648008(v=VS.85).aspx">Updating Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648043(v=VS.85).aspx">FindResourceEx</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648028(v=VS.85).aspx">IS_INTRESOURCE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646370(v=VS.85).aspx">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647990(v=VS.85).aspx">LoadMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647486(v=VS.85).aspx">LoadString</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648047(v=VS.85).aspx">LockResource</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632583(v=VS.85).aspx">Resources</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648048(v=VS.85).aspx">SizeofResource</a>
 

 

