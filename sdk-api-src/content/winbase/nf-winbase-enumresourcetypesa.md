---
UID: NF:winbase.EnumResourceTypesA
title: EnumResourceTypesA function (winbase.h)
description: Enumerates resource types within a binary module. (ANSI)
helpviewer_keywords: ["EnumResourceTypesA", "winbase/EnumResourceTypesA"]
old-location: menurc\enumresourcetypes.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcetypes.htm
ms.date: 12/05/2018
ms.keywords: EnumResourceTypes, EnumResourceTypes function [Menus and Other Resources], EnumResourceTypesA, EnumResourceTypesW, _win32_EnumResourceTypes, _win32_enumresourcetypes_cpp, menurc.enumresourcetypes, winbase/EnumResourceTypes, winbase/EnumResourceTypesA, winbase/EnumResourceTypesW, winui._win32_enumresourcetypes
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceTypesW (Unicode) and EnumResourceTypesA (ANSI)
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
 - EnumResourceTypesA
 - winbase/EnumResourceTypesA
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
 - EnumResourceTypes
 - EnumResourceTypesA
 - EnumResourceTypesW
---

# EnumResourceTypesA function


## -description

Enumerates resource types within a binary module. Starting with Windows Vista, this is typically a <a href="/windows/desktop/Intl/mui-resource-management">language-neutral Portable Executable</a> (LN file), and the enumeration also includes resources from one of the corresponding language-specific resource files (.mui files)—if one exists—that contain localizable language resources. It is also possible to use <i>hModule</i> to specify a .mui file, in which case only that file is searched for resource types.

Alternately, applications can call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw">EnumResourceTypesEx</a>, which provides more precise control over which resource files to enumerate.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to a module to be searched. This handle must be obtained through <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.
					
See Remarks for more information.

If this parameter is <b>NULL</b>, that is equivalent to passing in a handle to the module used to create the current process.

### -param lpEnumFunc [in]

Type: <b>ENUMRESTYPEPROC</b>

A pointer to the callback function to be called for each enumerated resource type. For more information, see the <a href="/windows/desktop/api/libloaderapi/nc-libloaderapi-enumrestypeprocw">EnumResTypeProc</a> function.

### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For each resource type found, <b>EnumResourceTypes</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing each resource type it finds, as well as the various other parameters that were passed to <b>EnumResourceTypes</b>.

<b>EnumResourceTypes</b> continues to enumerate resource types until the callback function returns <b>FALSE</b> or all resource types have been enumerated.

Starting with Windows Vista, if <i>hModule</i> specifies an LN file, then the types enumerated correspond to resources that reside in the LN file and in the .mui file associated with it. If no .mui files are found, only types from the LN file are returned. The order in which .mui files are searched is the usual Resource Loader search order; see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a> for details. After one appropriate .mui file is found, the search does not continue further to other .mui files associated with the LN file, because all .mui files that correspond to a single LN file have the same set of resource types.

The enumeration never includes duplicates: if a given resource type is contained in both the LN file and in an .mui file, the type is enumerated only once.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-resources">Creating a Resource List</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines EnumResourceTypes as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/libloaderapi/nc-libloaderapi-enumrestypeprocw">EnumResTypeProc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-enumresourcelanguagesa">EnumResourceLanguages</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesa">EnumResourceNames</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw">EnumResourceTypesEx</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>
