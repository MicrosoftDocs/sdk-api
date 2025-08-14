---
UID: NF:libloaderapi.EnumResourceTypesExW
title: EnumResourceTypesExW function (libloaderapi.h)
description: Enumerates resource types associated with a specified binary module. (Unicode)
helpviewer_keywords: ["EnumResourceTypesEx", "EnumResourceTypesEx function [Menus and Other Resources]", "EnumResourceTypesExW", "RESOURCE_ENUM_LN", "RESOURCE_ENUM_MUI", "RESOURCE_ENUM_VALIDATE", "_win32_EnumResourceTypesEx", "_win32_enumresourcetypesex_cpp", "libloaderapi/EnumResourceTypesEx", "libloaderapi/EnumResourceTypesExW", "menurc.enumresourcetypesex", "winui._win32_enumresourcetypesex"]
old-location: menurc\enumresourcetypesex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresourcetypesex.htm
ms.date: 12/05/2018
ms.keywords: EnumResourceTypesEx, EnumResourceTypesEx function [Menus and Other Resources], EnumResourceTypesExA, EnumResourceTypesExW, RESOURCE_ENUM_LN, RESOURCE_ENUM_MUI, RESOURCE_ENUM_VALIDATE, _win32_EnumResourceTypesEx, _win32_enumresourcetypesex_cpp, libloaderapi/EnumResourceTypesEx, libloaderapi/EnumResourceTypesExA, libloaderapi/EnumResourceTypesExW, menurc.enumresourcetypesex, winui._win32_enumresourcetypesex
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResourceTypesExW (Unicode) and EnumResourceTypesExA (ANSI)
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
 - EnumResourceTypesExW
 - libloaderapi/EnumResourceTypesExW
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
 - EnumResourceTypesEx
 - EnumResourceTypesExA
 - EnumResourceTypesExW
---

# EnumResourceTypesExW function


## -description

Enumerates resource types associated with a specified binary module. The search can include both a <a href="/windows/desktop/Intl/mui-resource-management">language-neutral Portable Executable</a> file (LN file) and its associated .mui files. Alternately, it can be limited to a single binary module of any type, or to the .mui files associated with a single LN file. The search can also be limited to a single associated .mui file that contains resources for a specific language.

      

For each resource type found, <b>EnumResourceTypesEx</b> calls an application-defined callback function <i>lpEnumFunc</i>, passing the resource type it finds, as well as the various other parameters that were passed to <b>EnumResourceTypesEx</b>.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

The handle to a module to be searched. Typically this is an LN file, and if flag <b>RESOURCE_ENUM_MUI</b> is set, then appropriate .mui files can be included in the search. Alternately, this can be a handle to an .mui file or other LN file.

If this parameter is <b>NULL</b>, it is equivalent to passing in a handle to the module used to create the current process.

### -param lpEnumFunc [in]

Type: <b>ENUMRESTYPEPROC</b>

A pointer to the callback function to be called for each enumerated resource type. For more information, see <a href="/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca">EnumResTypeProc</a>.

### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined value passed to the callback function.

### -param dwFlags [in]

Type: <b>DWORD</b>

The type of file to be searched. The following values are supported. Note that if <i>dwFlags</i> is zero, then the <b>RESOURCE_ENUM_LN</b> and <b>RESOURCE_ENUM_MUI</b>  flags are assumed to be specified.

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
Search for resource types in one of the .mui files associated with the file specified by <i>hModule</i> and with the current language preferences, following the usual Resource Loader strategy (see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>). Alternately, if <i>LangId</i> is nonzero, then only the .mui file of the language as specified by <i>LangId</i> will be searched. Typically this flag should be used only if <i>hModule</i> references an LN file. If <i>hModule</i> references an .mui file, then that file is actually covered by the <b>RESOURCE_ENUM_LN</b> flag, despite the name of the flag.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_LN"></a><a id="resource_enum_ln"></a><dl>
<dt><b>RESOURCE_ENUM_LN</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Searches only the file specified by <i>hModule</i>, regardless of whether the file is an LN file or an .mui file.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_ENUM_VALIDATE"></a><a id="resource_enum_validate"></a><dl>
<dt><b>RESOURCE_ENUM_VALIDATE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Performs extra validation on the resource section and its reference in the PE header while doing the enumeration to ensure that resources are properly formatted. The validation sets a maximum limit of 260 characters for each type that is enumerated.

</td>
</tr>
</table>

### -param LangId [in]

Type: <b>LANGID</b>

The language used to filter the search in the MUI module. This parameter is used only when the <b>RESOURCE_ENUM_MUI</b> flag is set in <i>dwFlags</i>. If zero is specified, then all .mui files that match current language preferences are included in the search, following the usual Resource Loader strategy (see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>). If a nonzero <i>LangId</i> is specified, then the only .mui file searched will be the one matching the specified <i>LangId</i>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful or <b>FALSE</b> if the function does not find a resource of the type specified, or if the function fails for another reason. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>EnumResourceTypesEx</b> function continues to enumerate resource types until the callback function returns <b>FALSE</b> or all resource types have been enumerated.

If <i>hModule</i> specifies an LN file, and both flags are selected, the types enumerated correspond to resources residing either in the LN file or in the .mui files associated with it. If no .mui files are found, only types from the LN file are returned. Once one appropriate .mui file is found the search will not continue further, because all .mui files corresponding to a single LN file have the same resource types.

If <i>dwFlags</i> and <i>LangId</i> are both zero, then the function behaves like <a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>.

If <i>LangId</i> is nonzero, then only the .mui file corresponding to that language identifier will be searched. Language fallbacks will not be used. If an .mui file for that language does not exist, the enumeration will be empty (unless resources for that language exist in the LN file, and the flag is set to search the LN file as well).

The enumeration never includes duplicates: if resources for a particular language are contained in both the LN file and in an .mui file, the type will only be enumerated once.


#### Examples

For an example, see <a href="/windows-hardware/drivers/wdf/creating-a-resource-requirements-list">Creating a Resource List</a>.

<div class="code"></div>




> [!NOTE]
> The libloaderapi.h header defines EnumResourceTypesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca">EnumResTypeProc</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa">EnumResourceLanguagesEx</a>



<a href="/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa">EnumResourceNamesEx</a>



<a href="/windows/win32/api/winbase/nf-winbase-enumresourcetypesa">EnumResourceTypes</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
