---
UID: NF:winnls.GetThreadPreferredUILanguages
title: GetThreadPreferredUILanguages function (winnls.h)
description: Retrieves the thread preferred UI languages for the current thread. For more information, see User Interface Language Management.
helpviewer_keywords: ["GetThreadPreferredUILanguages","GetThreadPreferredUILanguages function [Internationalization for Windows Applications]","MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","MUI_MERGE_SYSTEM_FALLBACK","MUI_MERGE_USER_FALLBACK","MUI_THREAD_LANGUAGES","MUI_UI_FALLBACK","_win32_GetThreadPreferredUILanguages","intl.getthreadpreferreduilanguages","winnls/GetThreadPreferredUILanguages"]
old-location: intl\getthreadpreferreduilanguages.htm
tech.root: Intl
ms.assetid: 8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d
ms.date: 12/05/2018
ms.keywords: GetThreadPreferredUILanguages, GetThreadPreferredUILanguages function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, MUI_MERGE_SYSTEM_FALLBACK, MUI_MERGE_USER_FALLBACK, MUI_THREAD_LANGUAGES, MUI_UI_FALLBACK, _win32_GetThreadPreferredUILanguages, intl.getthreadpreferreduilanguages, winnls/GetThreadPreferredUILanguages
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetThreadPreferredUILanguages
 - winnls/GetThreadPreferredUILanguages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetThreadPreferredUILanguages
---

# GetThreadPreferredUILanguages function


## -description

Retrieves the thread preferred UI languages for the current thread. For more information, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.

## -parameters

### -param dwFlags [in]

Flags identifying language format and filtering. The following flags specify the language format to use for the thread preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME. 

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
Retrieve the language strings in <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language strings in <a href="/windows/desktop/Intl/language-names">language name</a> format.

</td>
</tr>
</table>
 

The following flags specify filtering for the function to use in retrieving the thread preferred UI languages. The default flag is MUI_MERGE_USER_FALLBACK.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_MERGE_SYSTEM_FALLBACK"></a><a id="mui_merge_system_fallback"></a><dl>
<dt><b>MUI_MERGE_SYSTEM_FALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Use the system fallback to retrieve a list that corresponds exactly to the language list used by the resource loader. This flag can be used only in combination with MUI_MERGE_USER_FALLBACK. Using the flags in combination alters the usual effect of MUI_MERGE_USER_FALLBACK by including fallback and neutral languages in the list.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_MERGE_USER_FALLBACK"></a><a id="mui_merge_user_fallback"></a><dl>
<dt><b>MUI_MERGE_USER_FALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Retrieve a composite list consisting of the thread preferred UI languages, followed by process preferred UI languages, followed by any user preferred UI languages that are distinct from these, followed by the system default UI language, if it is not already in the list. If the user preferred UI languages list is empty, the function retrieves the system preferred UI languages. This flag cannot be combined with MUI_THREAD_LANGUAGES.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_THREAD_LANGUAGES"></a><a id="mui_thread_languages"></a><dl>
<dt><b>MUI_THREAD_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Retrieve only the thread preferred UI languages for the current thread, or an empty list if no preferred languages are set for the current thread. This flag cannot be combined with MUI_MERGE_USER_FALLBACK or MUI_MERGE_SYSTEM_FALLBACK.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_UI_FALLBACK"></a><a id="mui_ui_fallback"></a><dl>
<dt><b>MUI_UI_FALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Retrieve a complete thread preferred UI languages list along with associated fallback and neutral languages. Use of this flag is equivalent to combining MUI_MERGE_SYSTEM_FALLBACK and MUI_MERGE_USER_FALLBACK. (Applicable only for Windows 7 and later).

</td>
</tr>
</table>

### -param pulNumLanguages [out]

Pointer to the number of languages retrieved in <i>pwszLanguagesBuffer</i>.

### -param pwszLanguagesBuffer [out, optional]

Optional. Pointer to a buffer in which this function retrieves an ordered, null-delimited thread preferred UI languages list, in the format specified by <i>dwFlags</i>. This list ends with two null characters. 

Alternatively if this parameter is set to <b>NULL</b> and <i>pcchLanguagesBuffer</i> is set to 0, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. The required size includes the two null characters.

### -param pcchLanguagesBuffer [in, out]

Pointer to the size, in characters, for the language buffer indicated by <i>pwszLanguagesBuffer</i>. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and <i>pwszLanguagesBuffer</i> is set to <b>NULL</b>, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns one of the following error codes:
<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>


If the function fails for any other reason, the parameters <i>pulNumLanguages</i> and <i>pcchLanguagesBuffer</i> are undefined.

## -remarks

Depending on the flags specified by the application, this function can retrieve a composite list consisting of the thread preferred UI languages, process preferred UI languages, user preferred UI languages or system preferred UI languages, and the system default UI language. If it encounters a duplicate language, the function only retrieves the first language.

If the application has called <a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a> with the MUI_CONSOLE_FILTER or MUI_COMPLEX_SCRIPT_FILTER flag, <b>GetThreadPreferredUILanguages</b> filters the languages in the result list. The function replaces the languages the console cannot display with a substitute language. The substitution for a language is determined from the value of <a href="/windows/desktop/Intl/locale-sconsolefallbackname">LOCALE_SCONSOLEFALLBACKNAME</a> for the language. For more console information, see the description of <a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>.

Use of MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID because the MUI_LANGUAGE_NAME flag can do a better job of handling Language Interface Pack (LIP) languages that correspond to <a href="/windows/desktop/Intl/custom-locales">supplemental locales</a>.

When MUI_LANGUAGE_ID is specified, the language strings retrieved will be hexadecimal language identifiers 

that do not include the leading 0x, and will be 4 characters in length. For example, en-US will be returned 

as "0409" and en as "0009".

If the application sets the MUI_LANGUAGE_ID flag, the thread preferred UI languages can include one or more languages that correspond to supplemental locales. On successful return from the function, the language buffer contains "1400" for any language corresponding to a supplemental locale. There can be only one such language in this list. The string "1400" corresponds to the hexadecimal value of <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>. Also on successful return from the function, the <i>pwszLanguagesBuffer</i> contains "1000" for any other language that corresponds to a supplemental locale. The string "1000" corresponds to the hexadecimal value of <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>, which is not useful as an input to any function, because it cannot distinguish among supplemental locales.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetThreadPreferredUILanguages(
            System.UInt32 dwFlags,
            ref System.UInt32 pulNumLanguages,
            System.IntPtr pwszLanguagesBuffer,
            ref System.UInt32 pcchLanguagesBuffer
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getthreaduilanguage">GetThreadUILanguage</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>