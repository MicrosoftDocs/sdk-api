---
UID: NF:libloaderapi.EnumResourceNamesExW
title: EnumResourceNamesExW function (libloaderapi.h)
description: Enumerates resources of a specified type that are associated with a specified binary module. The search can include both an LN file and its associated .mui files, or it can be limited in several ways. (Unicode)
helpviewer_keywords: ["EnumResourceNamesEx", "EnumResourceNamesEx function [Menus and Other Resources]", "EnumResourceNamesExW", "RESOURCE_ENUM_LN", "RESOURCE_ENUM_MUI", "RESOURCE_ENUM_VALIDATE", "_win32_EnumResourceNamesEx", "_win32_enumresourcenamesex_cpp", "libloaderapi/EnumResourceNamesEx", "libloaderapi/EnumResourceNamesExW", "menurc.enumresourcenamesex", "winui._win32_enumresourcenamesex"]
old-location: menurc\enumresourcenamesex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcenamesex.htm
ms.date: 12/05/2018
ms.keywords: EnumResourceNamesEx, EnumResourceNamesEx function [Menus and Other Resources], EnumResourceNamesExA, EnumResourceNamesExW, RESOURCE_ENUM_LN, RESOURCE_ENUM_MUI, RESOURCE_ENUM_VALIDATE, _win32_EnumResourceNamesEx, _win32_enumresourcenamesex_cpp, libloaderapi/EnumResourceNamesEx, libloaderapi/EnumResourceNamesExA, libloaderapi/EnumResourceNamesExW, menurc.enumresourcenamesex, winui._win32_enumresourcenamesex
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceNamesExW (Unicode) and EnumResourceNamesExA (ANSI)
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
 - EnumResourceNamesExW
 - libloaderapi/EnumResourceNamesExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
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
 - EnumResourceNamesEx
 - EnumResourceNamesExA
 - EnumResourceNamesExW
---

## -description

Enumerates resources of a specified type that are associated with a specified binary module. The search can include both an LN file and its associated .mui files, or it can be limited in several ways.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

The handle to a module to search. Typically this is an LN file, and if flag <b>RESOURCE_ENUM_MUI</b> is set, then appropriate .mui files are included in the search. Alternately, this can be a handle to an .mui file or other LN file.

If this parameter is <b>NULL</b>, it is equivalent to passing in a handle to the module used to create the current process.

### -param lpType

Type: <b>LPCTSTR</b>

The type of the resource for which the name is being enumerated. Alternately, rather than a pointer, this parameter can be <a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(ID), where ID is an integer value representing a predefined resource type. For a list of predefined resource types, see <a href="https://msdn.microsoft.com/8d27f79a-8165-4565-a975-f25b2344efdc">Resource Types</a>. For more information, see the Remarks section below.

### -param lpEnumFunc [in]

Type: <b>ENUMRESNAMEPROC</b>

A pointer to the callback function to be called for each enumerated resource name. For more information, see <a href="/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca">EnumResNameProc</a>.

### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function. This parameter can be used in error checking.

### -param dwFlags [in]

Type: <b>DWORD</b>

The type of file to search. The following values are supported. Note that if <i>dwFlags</i> is zero, then the <b>RESOURCE_ENUM_LN</b> and <b>RESOURCE_ENUM_MUI</b>  flags are assumed to be specified.

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
Search for resources in .mui files associated with the LN file specified by <i>hModule</i> and with the current language preferences, following the usual Resource Loader strategy (see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>). Alternately, if <i>LangId</i> is nonzero, then only the specified .mui file will be searched. Typically this flag should be used only if <i>hModule</i> references an LN file. If <i>hModule</i> references an .mui file, then that file is actually covered by the <b>RESOURCE_ENUM_LN</b> flag, despite the name of the flag.

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
<td width="40%"><a id="RESOURCE_ENUM_VALIDATE"></a><a id="resource_enum_validate"></a><dl>
<dt><b>RESOURCE_ENUM_VALIDATE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Performs extra validation on the resource section and its reference in the PE header while doing the enumeration to ensure that resources are properly formatted. The validation sets a maximum limit of 260 characters for each name that is enumerated.

</td>
</tr>
</table>

### -param LangId [in]

Type: <b>LANGID</b>

The localization language used to filter the search in the MUI module. This parameter is used only when the <b>RESOURCE_ENUM_MUI</b> flag is set in <i>dwFlags</i>. If zero is specified, then all .mui files that match current language preferences are included in the search, following the usual Resource Loader strategy (see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>). If a nonzero <i>LangId</i> is specified, then the only .mui file searched will be the one matching the specified <i>LangId</i>.

## -returns

Type: <b>BOOL</b>

The function <b>TRUE</b> if successful, or <b>FALSE</b> if the function does not find a resource of the type specified, or if the function fails for another reason. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/windows/win32/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the 

integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

The enumeration search can include both an LN file and its associated .mui files. It can be limited to a single binary module of any type. It can also be limited to the .mui files associated with a single LN file. By specifying an LN file for the <i>hModule</i> parameter and a nonzero <i>LangId</i> parameter, the search can be limited to the unique .mui file associated with that LN file and language.

For each resource found, <b>EnumResourceNamesEx</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing the name or the ID of each resource it finds, as well as the various other parameters that were passed to <b>EnumResourceNamesEx</b>. The passed name is only valid inside the callback - if the passed name is a string pointer, it points to an internal buffer that is reused for all callback invocations.

If a resource has an ID, the ID is returned to the callback function; otherwise the resource name is returned to the callback function. For more information, see <a href="/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca">EnumResNameProc</a>.

The <b>EnumResourceNamesEx</b> function continues to enumerate resource names until the callback function returns <b>FALSE</b> or all resource names for this type have been enumerated.

If <i>hModule</i> specifies an LN file, and both flags are selected, the names enumerated correspond to resources residing either in that LN file or  the .mui files associated with it. If no .mui files are found, only names from the LN file are returned. After one appropriate .mui file is found the search will not continue further, because all .mui files corresponding to a single LN file have the same resource names.

If <i>dwFlags</i> and <i>LangId</i> are both zero, then the function behaves like <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesa">EnumResourceNames</a>.

If <i>LangId</i> is nonzero, then only the .mui file corresponding to that Language identifier will be searched. Language fallbacks will not be used. If an .mui file for that language does not exist, the enumeration will be empty (unless resources for that language exist in the LN file, and the flag is set to search the LN file as well).

The enumeration never includes duplicates: if resources for a particular language are contained in both the LN file and in an .mui file, the name will only be enumerated once.

## Examples

For an example, see <a href="/windows-hardware/drivers/wdf/creating-a-resource-requirements-list">Creating a Resource List</a>.

> [!NOTE]
> The libloaderapi.h header defines EnumResourceNamesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca">EnumResNameProc</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa">EnumResourceLanguagesEx</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesa">EnumResourceNames</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa">EnumResourceTypesEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
