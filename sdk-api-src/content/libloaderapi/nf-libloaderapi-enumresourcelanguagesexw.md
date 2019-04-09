---
UID: NF:libloaderapi.EnumResourceLanguagesExW
title: EnumResourceLanguagesExW function (libloaderapi.h)
author: windows-sdk-content
description: Enumerates language-specific resources, of the specified type and name, associated with a specified binary module. Extends EnumResourceLanguages by allowing more control over the enumeration.
old-location: menurc\enumresourcelanguagesex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcelanguagesex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumResourceLanguagesEx, EnumResourceLanguagesEx function [Menus and Other Resources], EnumResourceLanguagesExA, EnumResourceLanguagesExW, RESOURCE_ENUM_LN, RESOURCE_ENUM_MUI, RESOURCE_ENUM_MUI_SYSTEM, RESOURCE_ENUM_VALIDATE, _win32_EnumResourceLanguagesEx, _win32_enumresourcelanguagesex_cpp, libloaderapi/EnumResourceLanguagesEx, libloaderapi/EnumResourceLanguagesExA, libloaderapi/EnumResourceLanguagesExW, menurc.enumresourcelanguagesex, winui._win32_enumresourcelanguagesex
ms.topic: function
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceLanguagesExW (Unicode) and EnumResourceLanguagesExA (ANSI)
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
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - EnumResourceLanguagesEx
 - EnumResourceLanguagesExA
 - EnumResourceLanguagesExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumResourceLanguagesExW function


## -description


Enumerates language-specific resources, of the specified type and name, associated with a specified binary module. Extends <a href="https://msdn.microsoft.com/8e47d8df-e3ce-4125-aa77-8098a060f4aa">EnumResourceLanguages</a> by allowing more control over the enumeration.


## -parameters




### -param hModule [in]

Type: <b>HMODULE</b>

The handle to a module to search. Typically this is a <a href="https://msdn.microsoft.com/4d8b769d-0830-4e4e-b284-ce0b21dfe5d4">language-neutral Portable Executable</a> (LN file), and if flag <b>RESOURCE_ENUM_MUI</b> is set, then appropriate .mui files are included in the search. Alternately, this can be a handle to an .mui file or other LN file. If this is a specific .mui file, only that file is searched for resources.
    
                    

If this parameter is <b>NULL</b>, it is equivalent to passing in a handle to the module used to create the current process.


### -param lpType [in]

Type: <b>LPCTSTR</b>

The type of the resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. For a list of predefined resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. For more 

information, see the Remarks section below.


### -param lpName [in]

Type: <b>LPCTSTR</b>

The name of the resource for which the language is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the resource. For more information, see the Remarks section below.


### -param lpEnumFunc [in]

Type: <b>ENUMRESLANGPROC</b>

A pointer to the callback function to be called for each enumerated resource language. For more information, see <a href="https://msdn.microsoft.com/58c1a42d-15d2-4157-8c57-f9b1d389b917">EnumResLangProc</a>.


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function. This parameter can be used in error checking.


### -param dwFlags [in]

Type: <b>DWORD</b>

The type of file to be searched. The following values are supported. Note that if <i>dwFlags</i> is zero, then the <b>RESOURCE_ENUM_LN</b> and <b>RESOURCE_ENUM_MUI</b> flags are assumed to be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_MUI"></a><a id="resource_enum_mui"></a><dl>
<dt><b>RESOURCE_ENUM_MUI</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Search for language-specific resources in .mui files associated with the LN file specified by <i>hModule</i>. Alternately, if <i>LangId</i> is nonzero, the only .mui file searched will be the one matching the specified <i>LangId</i>. Typically this flag should be used only if <i>hModule</i> references an LN file. If <i>hModule</i> references an .mui file, then that file is actually covered by the <b>RESOURCE_LN</b> flag, despite the name of the flag. See the Remarks section below for sequence of search.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_LN"></a><a id="resource_enum_ln"></a><dl>
<dt><b>RESOURCE_ENUM_LN</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Searches the file specified by <i>hModule</i>, regardless of whether the file is an LN file, another type of LN file, or an .mui file.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_MUI_SYSTEM"></a><a id="resource_enum_mui_system"></a><dl>
<dt><b>RESOURCE_ENUM_MUI_SYSTEM</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Restricts the .mui files search to system-installed MUI languages.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_VALIDATE"></a><a id="resource_enum_validate"></a><dl>
<dt><b>RESOURCE_ENUM_VALIDATE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Performs extra validation on the resource section and its reference in the PE header while doing the enumeration to ensure that resources are properly formatted.

</td>
</tr>
</table>
 


### -param LangId [in]

Type: <b>LANGID</b>

The localization language used to filter the search in the .mui file. This parameter is used only when the <b>RESOURCE_ENUM_MUI</b> flag is set in <i>dwFlags</i>. If zero is specified, then all .mui files are included in the search. If a nonzero <i>LangId</i> is specified, then the only .mui file searched will be the one matching the specified <i>LangId</i>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> if the function does not find a resource of the type specified, or if the function fails for another reason. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpType</i>) is <b>TRUE</b>, then <i>lpType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the 

integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

Similarly, if <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpName</i>) is <b>TRUE</b>, then <i>lpName</i> specifies the integer identifier of the given resource. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the 

integer identifier of the resource.

Starting with Windows Vista, the binary module is typically an LN file, and the enumeration will also include resources from the corresponding language-specific resource files (.mui files) that contain localizable language resources.

For each such resource found, <b>EnumResourceLanguagesEx</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing to the callback function the language identifier (see <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>) of the language for which a resource was found (as well as the various other parameters that were passed to <b>EnumResourceLanguagesEx</b>).

The search can include both an LN file and its associated .mui files, or it can be limited either to a single binary module of any type, or to the .mui files associated with a single LN file. Also, by specifying an LN file for the <i>hModule</i> parameter and a nonzero <i>LangId</i> parameter, the search can be limited to the unique .mui file associated with that LN file and language.

The <b>EnumResourceLanguagesEx</b> function continues to enumerate resource languages until the callback function returns <b>FALSE</b> or all resource languages have been enumerated.

If <i>hModule</i> specifies an LN file, and both flags are selected, the languages enumerated include all languages whose resources reside either in the LN file or in any .mui files associated with it. If no .mui files are found, only languages from the LN file are returned.

If <i>dwFlags</i> contains <b>RESOURCE_ENUM_MUI</b> or <b>NULL</b> and <i>LangId</i> is 0, then the enumeration first includes the languages associated with all system-installed .mui files, using languages retrieved from <a href="https://msdn.microsoft.com/f97df853-fc40-4529-b8a5-27069863a9b9">EnumUILanguages</a>.. Finally, if the <b>RESOURCE_ENUM_LN</b> flag is also set, the file designated by <i>hModule</i> is also searched.

If the <i>LangId</i> is nonzero, then only the .mui file corresponding to that language identifier will be searched. Language fallbacks will not be used. If an .mui file for that language does not exist, the enumeration will be empty (unless resources for that language exist in the LN file, and the flag is set to search the LN file as well).

The enumeration never includes duplicates: if resources for a particular language are contained in both the LN file and in an .mui file, the type will only be enumerated once.


#### Examples

For an example, see <a href="using_resources.htm">Creating a Resource List</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58c1a42d-15d2-4157-8c57-f9b1d389b917">EnumResLangProc</a>



<a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a>



<a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

