---
UID: NF:winbase.EnumResourceNamesA
title: EnumResourceNamesA function (winbase.h)
description: Enumerates resources of a specified type within a binary module.
helpviewer_keywords: ["EnumResourceNames","EnumResourceNames function [Menus and Other Resources]","EnumResourceNamesA","EnumResourceNamesW","_win32_EnumResourceNames","_win32_enumresourcenames_cpp","menurc.enumresourcenames","winbase/EnumResourceNames","winbase/EnumResourceNamesA","winbase/EnumResourceNamesW","winui._win32_enumresourcenames"]
old-location: menurc\enumresourcenames.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcenames.htm
ms.date: 12/05/2018
ms.keywords: EnumResourceNames, EnumResourceNames function [Menus and Other Resources], EnumResourceNamesA, EnumResourceNamesW, _win32_EnumResourceNames, _win32_enumresourcenames_cpp, menurc.enumresourcenames, winbase/EnumResourceNames, winbase/EnumResourceNamesA, winbase/EnumResourceNamesW, winui._win32_enumresourcenames
f1_keywords:
- winbase/EnumResourceNames
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceNamesW (Unicode) and EnumResourceNamesA (ANSI)
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
- API-MS-Win-Core-LibraryLoader-L1-2-2.dll
- KernelBase.dll
api_name:
- EnumResourceNames
- EnumResourceNamesA
- EnumResourceNamesW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumResourceNamesA function


## -description


Enumerates resources of a specified type within a binary module. For Windows Vista and later, this is typically a <a href="https://docs.microsoft.com/windows/desktop/Intl/mui-resource-management">language-neutral Portable Executable</a> (LN file), and the enumeration will also include resources from the corresponding language-specific resource files (.mui files) that contain localizable language resources. It is also possible for <i>hModule</i> to specify an .mui file, in which case only that file is searched for resources.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to a module to be searched. Starting with Windows Vista, if this is an LN file, then appropriate .mui files (if any exist) are included in the search.

If this parameter is <b>NULL</b>, that is equivalent to passing in a handle to the module used to create the current process.


### -param lpType [in]

Type: <b>LPCTSTR</b>

The type of the resource for which the name is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. For a list of predefined resource types, see <a href="https://docs.microsoft.com/en-us/windows/win32/menurc/resource-types">Resource Types</a>. For more information, see 

the Remarks section below.


### -param lpEnumFunc [in]

Type: <b>ENUMRESNAMEPROC</b>

A pointer to the callback function to be called for each enumerated resource name or ID. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms648034(v=vs.85)">EnumResNameProc</a>.


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function. This parameter can be used in error checking.


## -returns



Type: <b>BOOL</b>

The return value is <b>TRUE</b> if the function succeeds or <b>FALSE</b> if the function does not find a resource of the type specified, or if the function fails for another reason. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the 

integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

For each resource found, <b>EnumResourceNames</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing the name or the ID of each resource it finds, as well as the various other parameters that were passed to <b>EnumResourceNames</b>.

Alternately, applications can call <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw">EnumResourceNamesEx</a>, which provides more precise control of what resources are enumerated.

If a resource has an ID, the ID is passed to the callback function; otherwise the resource name is passed to the callback function. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms648034(v=vs.85)">EnumResNameProc</a>.

The <b>EnumResourceNames</b> function continues to enumerate resources until the callback function returns <b>FALSE</b> or all resources have been enumerated.

Starting with Windows Vista, if <i>hModule</i> specifies an LN file, then the resources enumerated can reside either in the LN file or in a .mui file associated with it. If no .mui files are found, only resources from the LN file are returned. The order in which .mui files are searched is the usual Resource Loader search order; see <a href="https://docs.microsoft.com/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a> for details. Once one appropriate .mui file is found, the .mui file search stops. Because all .mui files that correspond to a single LN file have the same resource types, only the resources in the found .mui file need to be enumerated.

The enumeration never includes duplicates: if resources with the same name are contained in both the LN file and in an .mui file, the resource will only be enumerated once.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-resources">Creating a Resource List</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms648034(v=vs.85)">EnumResNameProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-enumresourcelanguagesa">EnumResourceLanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw">EnumResourceNamesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/resources">Resources</a>
 

 

