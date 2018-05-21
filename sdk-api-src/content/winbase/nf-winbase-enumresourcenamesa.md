---
UID: NF:winbase.EnumResourceNamesA
title: EnumResourceNamesA function
author: windows-driver-content
description: Enumerates resources of a specified type within a binary module.
old-location: menurc\enumresourcenames.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcenames.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: EnumResourceNames, EnumResourceNames function [Menus and Other Resources], EnumResourceNamesA, EnumResourceNamesW, _win32_EnumResourceNames, _win32_enumresourcenames_cpp, menurc.enumresourcenames, winbase/EnumResourceNames, winbase/EnumResourceNamesA, winbase/EnumResourceNamesW, winui._win32_enumresourcenames
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
req.unicode-ansi: EnumResourceNamesW (Unicode) and EnumResourceNamesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-LibraryLoader-L1-2-2.dll
-	KernelBase.dll
api_name:
-	EnumResourceNames
-	EnumResourceNamesA
-	EnumResourceNamesW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumResourceNamesA function


## -description


Enumerates resources of a specified type within a binary module. For Windows Vista and later, this is typically a <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">language-neutral Portable Executable</a> (LN file), and the enumeration will also include resources from the corresponding language-specific resource files (.mui files) that contain localizable language resources. It is also possible for <i>hModule</i> to specify an .mui file, in which case only that file is searched for resources.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to a module to be searched. Starting with Windows Vista, if this is an LN file, then appropriate .mui files (if any exist) are included in the search.

If this parameter is <b>NULL</b>, that is equivalent to passing in a handle to the module used to create the current process.


### -param lpType

TBD


### -param lpEnumFunc [in]

Type: <b>ENUMRESNAMEPROC</b>

A pointer to the callback function to be called for each enumerated resource name or ID. For more information, see <a href="https://msdn.microsoft.com/286118cd-8832-4e8f-92c7-aa1ab34e66c5">EnumResNameProc</a>.


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function. This parameter can be used in error checking.


#### - lpszType [in]

Type: <b>LPCTSTR</b>

The type of the resource for which the name is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. For a list of predefined resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. For more information, see 

the Remarks section below.


## -returns



Type: <b>BOOL</b>

The return value is <b>TRUE</b> if the function succeeds or <b>FALSE</b> if the function does not find a resource of the type specified, or if the function fails for another reason. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the 

integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

For each resource found, <b>EnumResourceNames</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing the name or the ID of each resource it finds, as well as the various other parameters that were passed to <b>EnumResourceNames</b>.

Alternately, applications can call <a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a>, which provides more precise control of what resources are enumerated.

If a resource has an ID, the ID is passed to the callback function; otherwise the resource name is passed to the callback function. For more information, see <a href="https://msdn.microsoft.com/286118cd-8832-4e8f-92c7-aa1ab34e66c5">EnumResNameProc</a>.

The <b>EnumResourceNames</b> function continues to enumerate resources until the callback function returns <b>FALSE</b> or all resources have been enumerated.

Starting with Windows Vista, if <i>hModule</i> specifies an LN file, then the resources enumerated can reside either in the LN file or in a .mui file associated with it. If no .mui files are found, only resources from the LN file are returned. The order in which .mui files are searched is the usual Resource Loader search order; see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a> for details. Once one appropriate .mui file is found, the .mui file search stops. Because all .mui files that correspond to a single LN file have the same resource types, only the resources in the found .mui file need to be enumerated.

The enumeration never includes duplicates: if resources with the same name are contained in both the LN file and in an .mui file, the resource will only be enumerated once.


#### Examples

For an example, see <a href="using_resources.htm">Creating a Resource List</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/286118cd-8832-4e8f-92c7-aa1ab34e66c5">EnumResNameProc</a>



<a href="https://msdn.microsoft.com/8e47d8df-e3ce-4125-aa77-8098a060f4aa">EnumResourceLanguages</a>



<a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a>



<a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

