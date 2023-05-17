---
UID: NF:winbase.EnumResourceLanguagesA
title: EnumResourceLanguagesA function (winbase.h)
description: Enumerates language-specific resources, of the specified type and name, associated with a binary module. (ANSI)
helpviewer_keywords: ["EnumResourceLanguagesA", "winbase/EnumResourceLanguagesA"]
old-location: menurc\enumresourcelanguages.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcelanguages.htm
ms.date: 12/05/2018
ms.keywords: EnumResourceLanguages, EnumResourceLanguages function [Menus and Other Resources], EnumResourceLanguagesA, EnumResourceLanguagesW, _win32_EnumResourceLanguages, _win32_enumresourcelanguages_cpp, menurc.enumresourcelanguages, winbase/EnumResourceLanguages, winbase/EnumResourceLanguagesA, winbase/EnumResourceLanguagesW, winui._win32_enumresourcelanguages
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceLanguagesW (Unicode) and EnumResourceLanguagesA (ANSI)
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
 - EnumResourceLanguagesA
 - winbase/EnumResourceLanguagesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - EnumResourceLanguages
 - EnumResourceLanguagesA
 - EnumResourceLanguagesW
---

# EnumResourceLanguagesA function


## -description

Enumerates language-specific resources, of the specified type and name, associated with a binary module.

## -parameters

### -param hModule [in]

Type: <b>HMODULE</b>

The handle to a module to be searched. Starting with Windows Vista, if this is a <a href="/windows/desktop/Intl/mui-resource-management">language-neutral Portable Executable</a> (LN file), then appropriate .mui files (if any exist) are included in the search. If this is a specific .mui file, only that file is searched for resources.
				
                    

If this parameter is <b>NULL</b>, that is equivalent to passing in a handle to the module used to create the current process.

### -param lpType [in]

Type: <b>LPCTSTR</b>

The type of resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. For a list of predefined resource types, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Resource Types</a>. For more information, see the Remarks section below.

### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.

### -param lpEnumFunc [in]

Type: <b>ENUMRESLANGPROC</b>

A pointer to the callback function to be called for each enumerated resource language. For more information, see <a href="/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)">EnumResLangProc</a>.

### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function. This parameter can be used in error checking.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>lpType</i>) is <b>TRUE</b>, then <i>lpType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

Similarly, if <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>lpName</i>) is <b>TRUE</b>, then <i>lpName</i> specifies the integer identifier of the given resource. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource.

Starting with Windows Vista, the binary module is typically a <a href="/windows/desktop/Intl/mui-resource-management">language-neutral Portable Executable</a> (LN file), and the enumeration will also include resources from the corresponding language-specific resource files (.mui files) that contain localizable language resources.

For each resource found, <b>EnumResourceLanguages</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing the language identifier (see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>) of the language for which a resource was found, as well as the various other parameters that were passed to <b>EnumResourceLanguages</b>.

Alternately, applications can call <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw">EnumResourceLanguagesEx</a>, which provides more precise control of what resources are enumerated.

The <b>EnumResourceLanguages</b> function continues to enumerate resource languages until the callback function returns <b>FALSE</b> or all resource languages have been enumerated.

In Windows Vista and later, if  <i>hModule</i> specifies an LN file, then the resources enumerated can reside either in the LN file or in an .mui file associated with it.  If no .mui files are found, only resources from the LN file are returned.  Unlike <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesa">EnumResourceNames</a> and <a href="/windows/desktop/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>, this search will look at multiple .mui files. The enumeration begins with .mui files in the folders associated with <a href="/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a>. These are followed by any other .mui files whose paths conform to the scheme described at <a href="/windows/desktop/Intl/mui-resource-management">MUI Resource Management</a>. Finally, the file designated by <i>hModule</i> is also searched.

The enumeration never includes duplicates: if a resource with the same name, type, and language is contained in both the LN file and in an .mui file, the resource will only be enumerated once.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-resources">Creating a Resource List</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines EnumResourceLanguages as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/previous-versions/windows/desktop/legacy/ms648033(v=vs.85)">EnumResLangProc</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw">EnumResourceLanguagesEx</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesa">EnumResourceNames</a>



<a href="/windows/desktop/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>
