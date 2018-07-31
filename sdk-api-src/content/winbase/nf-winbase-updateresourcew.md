---
UID: NF:winbase.UpdateResourceW
title: UpdateResourceW function
author: windows-sdk-content
description: Adds, deletes, or replaces a resource in a portable executable (PE) file.
old-location: menurc\updateresource.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\updateresource.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UpdateResource, UpdateResource function [Menus and Other Resources], UpdateResourceA, UpdateResourceW, _win32_UpdateResource, _win32_updateresource_cpp, menurc.updateresource, winbase/UpdateResource, winbase/UpdateResourceA, winbase/UpdateResourceW, winui._win32_updateresource
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
req.unicode-ansi: UpdateResourceW (Unicode) and UpdateResourceA (ANSI)
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
api_name:
 - UpdateResource
 - UpdateResourceA
 - UpdateResourceW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# UpdateResourceW function


## -description


Adds, deletes, or replaces a resource in a portable executable (PE) file. There are some restrictions on resource updates in files that contain Resource Configuration (RC Config) data: <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">language-neutral</a> (LN) files and language-specific resource (.mui) files.


## -parameters




### -param hUpdate [in]

Type: <b>HANDLE</b>

A module handle returned by the <a href="https://msdn.microsoft.com/7702a24d-b786-47ae-9d7e-d047fbb50a7e">BeginUpdateResource</a> function, referencing the file to be updated. 


### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type to be updated. Alternatively, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. If the first character of the string is a pound sign (#), then the remaining characters represent a 

decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258. 

For a list of predefined resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. 


### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource to be updated. Alternatively, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is a resource ID. When creating a new resource do not use a string that begins with a '#' character for this parameter.


### -param wLanguage [in]

Type: <b>WORD</b>

The <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the resource to be updated. For a list of the primary language identifiers and sublanguage identifiers that make up a language identifier, see the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>  macro. 


### -param lpData [in, optional]

Type: <b>LPVOID</b>

The resource data to be inserted into the file indicated by <i>hUpdate</i>. If the resource is one of the predefined types, the data must be valid and properly aligned. Note that this is the raw binary data to be stored in the file indicated by <i>hUpdate</i>, not the data provided by <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>, <a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>, or other resource-specific load functions. All data containing strings or text must be in Unicode format. <i>lpData</i> must not point to ANSI data.

    				

If <i>lpData</i> is <b>NULL</b> and <i>cbData</i> is 0, the specified resource is deleted from the file indicated by <i>hUpdate</i>.


### -param cb

TBD




#### - cbData [in]

Type: <b>DWORD</b>

The size, in bytes, of the resource data at <i>lpData</i>. 


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



It is recommended that the resource file is not loaded before this function is called. However, if that file is already loaded, it will not cause an error to be returned.

An application can use <b>UpdateResource</b> repeatedly to make changes to the resource data. Each call to <b>UpdateResource</b> contributes to an internal list of additions, deletions, and replacements but does not actually write the data to the file indicated by <i>hUpdate</i>. The application must use the <a href="https://msdn.microsoft.com/19d251ec-ee98-4455-a091-e2e4a3b80092">EndUpdateResource</a> function to write the accumulated changes to the file.

This function can update resources within modules that contain both code and resources.

<b>Prior to Windows 7:</b> If <i>lpData</i> is <b>NULL</b> and <i>cbData</i> is nonzero, the specified resource is NOT deleted and an exception is thrown.

<b>Starting with Windows Vista:</b> As noted above, there are restrictions on resource updates in files that contain RC Config data: LN files and .mui files. The restrictions are as follows:

<table class="clsStd">
<tr>
<th>Action</th>
<th>LN file</th>
<th>.mui file</th>
</tr>
<tr>
<td>1. Add a new type that doesn't exist in the LN or .mui files.</td>
<td>Add type in the LN file and treat as language-neutral (non-localizable) and add new type or item in the RC Config data</td>
<td>The only additions allowed are the following types: file Version, RC Config data, Side-by-side Assembly XML Manifest.</td>
</tr>
<tr>
<td>2. Add a new resource item to an existing type.</td>
<td>Uses the RC Config data to check whether the type exists in the .mui files associated with this LN file. If the type doesn't exist in the .mui files, add the item and treat new item as un-localizable. If the type exists in the .mui files, then adding is not allowed.</td>
<td>Only items of the following types may be added: File Version, RC Config data, Side-by-side Assembly XML Manifest.</td>
</tr>
<tr>
<td>3. Update a resource item.</td>
<td>Uses the RC Config data to check whether the type exists in the .mui files associated with the LN file. If the type doesn't exist in the .mui files, then this resource item update is allowed in the LN file. Otherwise, if the type exists in the .mui files associated with this LN file, then this update is not allowed.</td>
<td>The only updates allowed are items of the following types: file Version, RC Config data, Side-by-side Assembly XML Manifest.</td>
</tr>
<tr>
<td>4. Add a type/item for a new language.</td>
<td>Not allowed.</td>
<td>Not allowed.</td>
</tr>
<tr>
<td>5. Remove an existing type/item.</td>
<td>Works similarly to case 3. Uses the RC Config data to check whether the type exists in the .mui files associated with the LN file. If not, then the removal of the type/item from the LN file is allowed.  Otherwise, if the type/item exists in the .mui files associated with this LN file, then the removal is not allowed.</td>
<td>The only types allowed to be removed are: file Version, RC Config data, Side-by-side Assembly XML Manifest; also, only items of these types may be removed.</td>
</tr>
<tr>
<td>6. Add/delete/update a type not included in the RC Config data (such as Version, Side-by-side Assembly XML Manifest, or RC Config data itself). </td>
<td>Allowed.</td>
<td>Allowed.</td>
</tr>
<tr>
<td>7. Other update of non-localizable data, such as TYPELIB, reginst, and so on.</td>
<td>Update type or item in the LN file, treat as non-localizable, and add new type or item in the RC Config data.</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>8. Add RC Config data.</td>
<td>Can be done but the integrity of the RC Config data is not checked.</td>
<td>Can be done but the integrity of the RC Config data is not checked.</td>
</tr>
</table>
 


#### Examples

For an example, see <a href="using_resources.htm">Updating Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7702a24d-b786-47ae-9d7e-d047fbb50a7e">BeginUpdateResource</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/19d251ec-ee98-4455-a091-e2e4a3b80092">EndUpdateResource</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/9d878af7-a7b1-4d24-89ff-c567e4a8accd">LoadString</a>



<a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>



<a href="https://msdn.microsoft.com/e3eb82a3-15b6-4874-81d3-955d38d42383">SizeofResource</a>
 

 

