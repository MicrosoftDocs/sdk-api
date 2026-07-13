---
UID: NF:muiload.LoadMUILibraryA
title: LoadMUILibraryA function (muiload.h)
description: Returns a handle to the language-specific resources associated with a particular language-neutral (LN) file. (ANSI)
helpviewer_keywords: ["LoadMUILibraryA", "MUI_LANGUAGE_EXACT", "MUI_LANGUAGE_ID", "MUI_LANGUAGE_NAME", "muiload/LoadMUILibraryA"]
old-location: intl\loadmuilibrary.htm
tech.root: Intl
ms.assetid: 277067d8-c38d-4e79-9c1a-4e4af1987228
ms.date: 12/05/2018
ms.keywords: LoadMUILibrary, LoadMUILibrary function [Internationalization for Windows Applications], LoadMUILibraryA, LoadMUILibraryW, MUI_LANGUAGE_EXACT, MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, _win32_LoadMUILibrary, intl.loadmuilibrary, muiload/LoadMUILibrary, muiload/LoadMUILibraryA, muiload/LoadMUILibraryW
req.header: muiload.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMUILibraryW (Unicode) and LoadMUILibraryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Muiload.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Muiload.lib, included in the Windows SDK for Windows 7 which can be run on Windows 2000 Professional, Windows 2000 Server, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7.
ms.custom: 19H1
f1_keywords:
 - LoadMUILibraryA
 - muiload/LoadMUILibraryA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Muiload.lib
api_name:
 - LoadMUILibrary
 - LoadMUILibraryA
 - LoadMUILibraryW
---

# LoadMUILibraryA function


## -description

Returns a handle to the language-specific resources associated with a particular language-neutral (LN) file.
<div class="alert"><b>Note</b>  To ensure that the DLL is unloaded correctly, your applications should match each call to <b>LoadMUILibrary</b> with a corresponding call to <a href="/windows/desktop/api/muiload/nf-muiload-freemuilibrary">FreeMUILibrary</a>.</div><div> </div>

## -parameters

### -param pszFullModuleName [in]

Pointer to a null-terminated string specifying the name of an LN file.

### -param dwLangConvention [in]

Flags specifying the naming convention on pre-Windows Vista operating systems to name the directories containing the language-specific resource files. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_ID"></a><a id="mui_language_id"></a><dl>
<dt><b>MUI_LANGUAGE_ID</b></dt>
</dl>
</td>
<td width="60%">
Interpret the name of the folder containing the language-specific resource files using <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Interpret the name of the folder containing the language-specific resource files using <a href="/windows/desktop/Intl/language-names">language name</a> format.

</td>
</tr>
</table>
 

The following flag is available as an option and can be used in combination with either of the other flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_EXACT"></a><a id="mui_language_exact"></a><dl>
<dt><b>MUI_LANGUAGE_EXACT</b></dt>
</dl>
</td>
<td width="60%">
If resources for the identified language are not found in the resource files, check the main module specified by <i>pwszModuleName</i> and return a handle to that module if successful. 
	

</td>
</tr>
</table>

### -param LangID [in]

Language identifier for the user interface resources on a pre-Windows Vista operating system. The language identifier cannot correspond to the language associated with any of these locale information constants: 


<ul>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

## -returns

Returns a handle to the appropriate language-specific resource file if successful.

This function returns <b>NULL</b> if it fails. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function allows applications developed using the Win32 MUI resource technology to determine correctly the language-specific resource file to load on pre-Windows Vista operating systems. Applications using this function do not specifically have to be built on Windows Vista, but they do have to link statically with the MUILoad library provided in the Microsoft Windows SDK for Windows Vista. This function requires the executable and language-specific resource files to be stored using standard conventions. See <a href="/windows/desktop/Intl/application-deployment">Application Deployment</a> for further information about file placement.

The following items influence the loading of satellite binaries by this function.

<ul>
<li>Operating system version running the application that calls the function</li>
<li>Flag passed in the <i>dwLangConvention</i> parameter</li>
<li>State of the language identifier passed in the <i>LangID</i> parameter</li>
</ul>
When running on Windows Vista, this function loads the main module without redirection. Only the <i>pszFullModuleName</i> parameter is used, as the resource loader functions perform redirection appropriately when they are called. When running on pre-Windows Vista operating systems, this function takes into account all parameters that the application supplies. It redirects binary loading to the proper satellite binary pair associated with the file represented by <i>pszFullModuleName</i>. This process reconstitutes the path associated with the file to mimic the behavior of Windows Vista that underlies the resource loader functions.

The application uses the <i>dwLangConvention</i> parameter to specify the way the satellite binaries should be probed. If the application sets this parameter to MUI_LANGUAGE_ID, the binaries are probed in folders with hexadecimal string values. (These values do not include the leading 0x, and are 4 characters in length. For example, en-US is represented 

as "0409" and en as "0009".) If the application sets the parameter to MUI_LANGUAGE_NAME, the function uses Windows Vista resource loading, which uses language name-based folder probes to find a satellite file.

The state of the language identifier in the <i>LangID</i> parameter affects resource probing. If the application sets this parameter to 0, the function uses the predefined fallback logic, dependent on the operating system, to locate the appropriate language-specific resource file. When the application sets <i>LangID</i> to a nonzero value, the probing mechanism only searches the appropriately named folder and its associated neutral equivalent. For more information, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.

<b>LoadMUILibrary</b> is built on the function <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>, and similar considerations need to be applied to its usage. In particular, <a href="/windows/desktop/api/muiload/nf-muiload-freemuilibrary">FreeMUILibrary</a> should be called for any handle returned by <b>LoadMUILibrary</b>. Also, <b>LoadMUILibrary</b> should not be called from <a href="/windows/desktop/Dlls/dllmain">DllMain</a>. For more information see the Remarks sections of <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>.





> [!NOTE]
> The muiload.h header defines LoadMUILibrary as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/muiload/nf-muiload-freemuilibrary">FreeMUILibrary</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>
