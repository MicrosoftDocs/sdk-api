---
UID: NF:winbase.UpdateResourceA
title: UpdateResourceA function (winbase.h)
description: Adds, deletes, or replaces a resource in a portable executable (PE) file. (ANSI)
helpviewer_keywords: ["UpdateResourceA", "winbase/UpdateResourceA"]
old-location: menurc\updateresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\updateresource.htm
ms.date: 12/05/2018
ms.keywords: UpdateResource, UpdateResource function [Menus and Other Resources], UpdateResourceA, UpdateResourceW, _win32_UpdateResource, _win32_updateresource_cpp, menurc.updateresource, winbase/UpdateResource, winbase/UpdateResourceA, winbase/UpdateResourceW, winui._win32_updateresource
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdateResourceA
 - winbase/UpdateResourceA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-kernel32-updateresource-l1-1-0.dll
 - Kernel32.dll
api_name:
 - UpdateResource
 - UpdateResourceA
 - UpdateResourceW
---

# UpdateResourceA function


## -description

Adds, deletes, or replaces a resource in a portable executable (PE) file. There are some restrictions on resource updates in files that contain Resource Configuration (RC Config) data: <a href="/windows/desktop/Intl/mui-resource-management">language-neutral</a> (LN) files and language-specific resource (.mui) files.

## -parameters

### -param hUpdate [in]

Type: <b>HANDLE</b>

A module handle returned by the <a href="/windows/desktop/api/winbase/nf-winbase-beginupdateresourcea">BeginUpdateResource</a> function, referencing the file to be updated.

### -param lpType [in]

Type: <b>LPCTSTR</b>

The resource type to be updated. Alternatively, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

For a list of predefined resource types, see <a href="/windows/win32/menurc/resource-types">Resource Types</a>.

### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource to be updated. Alternatively, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is a resource ID. When creating a new resource do not use a string that begins with a '#' character for this parameter.

### -param wLanguage [in]

Type: <b>WORD</b>

The <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> of the resource to be updated. For a list of the primary language identifiers and sublanguage identifiers that make up a language identifier, see the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>  macro.

### -param lpData [in, optional]

Type: <b>LPVOID</b>

The resource data to be inserted into the file indicated by <i>hUpdate</i>. If the resource is one of the predefined types, the data must be valid and properly aligned. Note that this is the raw binary data to be stored in the file indicated by <i>hUpdate</i>, not the data provided by <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>, or other resource-specific load functions. All data containing strings or text must be in Unicode format. <i>lpData</i> must not point to ANSI data.

    				

If <i>lpData</i> is <b>NULL</b> and <i>cbData</i> is 0, the specified resource is deleted from the file indicated by <i>hUpdate</i>.

### -param cb [in]

Type: <b>DWORD</b>

The size, in bytes, of the resource data at <i>lpData</i>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

It is recommended that the resource file is not loaded before this function is called. However, if that file is already loaded, it will not cause an error to be returned.

An application can use <b>UpdateResource</b> repeatedly to make changes to the resource data. Each call to <b>UpdateResource</b> contributes to an internal list of additions, deletions, and replacements but does not actually write the data to the file indicated by <i>hUpdate</i>. The application must use the <a href="/windows/desktop/api/winbase/nf-winbase-endupdateresourcea">EndUpdateResource</a> function to write the accumulated changes to the file.

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

For an example, see <a href="/windows/desktop/menurc/using-resources">Updating Resources</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines UpdateResource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-beginupdateresourcea">BeginUpdateResource</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winbase/nf-winbase-endupdateresourcea">EndUpdateResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-sizeofresource">SizeofResource</a>
