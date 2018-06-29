---
UID: NF:winbase.EnumResourceTypesA
title: EnumResourceTypesA function
author: windows-sdk-content
description: Enumerates resource types within a binary module.
old-location: menurc\enumresourcetypes.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcetypes.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: EnumResourceTypes, EnumResourceTypes function [Menus and Other Resources], EnumResourceTypesA, EnumResourceTypesW, _win32_EnumResourceTypes, _win32_enumresourcetypes_cpp, menurc.enumresourcetypes, winbase/EnumResourceTypes, winbase/EnumResourceTypesA, winbase/EnumResourceTypesW, winui._win32_enumresourcetypes
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
req.unicode-ansi: EnumResourceTypesW (Unicode) and EnumResourceTypesA (ANSI)
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
 - EnumResourceTypes
 - EnumResourceTypesA
 - EnumResourceTypesW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumResourceTypesA function


## -description


Enumerates resource types within a binary module. Starting with Windows Vista, this is typically a <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">language-neutral Portable Executable</a> (LN file), and the enumeration also includes resources from one of the corresponding language-specific resource files (.mui files)—if one exists—that contain localizable language resources. It is also possible to use <i>hModule</i> to specify a .mui file, in which case only that file is searched for resource types.

Alternately, applications can call <a href="https://msdn.microsoft.com/library/ms648040(v=VS.85).aspx">EnumResourceTypesEx</a>, which provides more precise control over which resource files to enumerate.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to a module to be searched. This handle must be obtained through <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> or <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>.
					
                    See Remarks for more information.

If this parameter is <b>NULL</b>, that is equivalent to passing in a handle to the module used to create the current process.


### -param lpEnumFunc [in]

Type: <b>ENUMRESTYPEPROC</b>

A pointer to the callback function to be called for each enumerated resource type. For more information, see the <a href="https://msdn.microsoft.com/library/ms648041(v=VS.85).aspx">EnumResTypeProc</a> function.


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For each resource type found, <b>EnumResourceTypes</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing each resource type it finds, as well as the various other parameters that were passed to <b>EnumResourceTypes</b>.

<b>EnumResourceTypes</b> continues to enumerate resource types until the callback function returns <b>FALSE</b> or all resource types have been enumerated.

Starting with Windows Vista, if <i>hModule</i> specifies an LN file, then the types enumerated correspond to resources that reside in the LN file and in the .mui file associated with it. If no .mui files are found, only types from the LN file are returned. The order in which .mui files are searched is the usual Resource Loader search order; see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a> for details. After one appropriate .mui file is found, the search does not continue further to other .mui files associated with the LN file, because all .mui files that correspond to a single LN file have the same set of resource types.

The enumeration never includes duplicates: if a given resource type is contained in both the LN file and in an .mui file, the type is enumerated only once.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/library/ms648008(v=VS.85).aspx">Creating a Resource List</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms648041(v=VS.85).aspx">EnumResTypeProc</a>



<a href="https://msdn.microsoft.com/library/ms648035(v=VS.85).aspx">EnumResourceLanguages</a>



<a href="https://msdn.microsoft.com/library/ms648037(v=VS.85).aspx">EnumResourceNames</a>



<a href="https://msdn.microsoft.com/library/ms648040(v=VS.85).aspx">EnumResourceTypesEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms632583(v=VS.85).aspx">Resources</a>
 

 

