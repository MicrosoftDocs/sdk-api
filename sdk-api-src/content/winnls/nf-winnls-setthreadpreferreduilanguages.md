---
UID: NF:winnls.SetThreadPreferredUILanguages
title: SetThreadPreferredUILanguages function (winnls.h)
description: Sets the thread preferred UI languages for the current thread. For more information, see User Interface Language Management.
helpviewer_keywords: ["MUI_COMPLEX_SCRIPT_FILTER","MUI_CONSOLE_FILTER","MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","MUI_RESET_FILTERS","SetThreadPreferredUILanguages","SetThreadPreferredUILanguages function [Internationalization for Windows Applications]","_win32_SetThreadPreferredUILanguages","intl.setthreadpreferreduilanguages","winnls/SetThreadPreferredUILanguages"]
old-location: intl\setthreadpreferreduilanguages.htm
tech.root: Intl
ms.assetid: 32a8117c-2cb2-4559-8e86-9fad5b28aa5b
ms.date: 12/05/2018
ms.keywords: MUI_COMPLEX_SCRIPT_FILTER, MUI_CONSOLE_FILTER, MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, MUI_RESET_FILTERS, SetThreadPreferredUILanguages, SetThreadPreferredUILanguages function [Internationalization for Windows Applications], _win32_SetThreadPreferredUILanguages, intl.setthreadpreferreduilanguages, winnls/SetThreadPreferredUILanguages
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
 - SetThreadPreferredUILanguages
 - winnls/SetThreadPreferredUILanguages
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetThreadPreferredUILanguages
---

# SetThreadPreferredUILanguages function


## -description

Sets the thread preferred UI languages for the current thread. For more information, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.


<div class="alert"><b>Note</b>  This function is also used by the operating system to identify languages that are safe to use on the Windows console.</div>
<div> </div>

## -parameters

### -param dwFlags [in]

Flags identifying format and filtering for the languages to set. 

The following <i>format flags</i> specify the language format to use for the thread preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

We recommend that you use MUI_LANGUAGE_NAME instead of MUI_LANGUAGE_ID.

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
The input parameter language strings are in <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The input parameter language strings are in <a href="/windows/desktop/Intl/language-names">language name</a> format.

</td>
</tr>
</table>
 

The following <i>filtering flags</i> specify filtering for the language list. The flags are mutually exclusive. By default, neither MUI_COMPLEX_SCRIPT_FILTER nor MUI_CONSOLE_FILTER is set. For more information about the filtering flags, see the Remarks section.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_COMPLEX_SCRIPT_FILTER"></a><a id="mui_complex_script_filter"></a><dl>
<dt><b>MUI_COMPLEX_SCRIPT_FILTER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> should replace with the appropriate fallback all languages having <a href="/windows/desktop/Intl/uniscribe-glossary">complex scripts</a>. When this flag is specified, <b>NULL</b> must be passed for all other parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_CONSOLE_FILTER"></a><a id="mui_console_filter"></a><dl>
<dt><b>MUI_CONSOLE_FILTER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> should replace with the appropriate fallback all languages that cannot display properly in a console window with the current operating system settings. When this flag is specified, <b>NULL</b> must be passed for all other parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_RESET_FILTERS"></a><a id="mui_reset_filters"></a><dl>
<dt><b>MUI_RESET_FILTERS</b></dt>
</dl>
</td>
<td width="60%">
Reset the filtering for the language list by removing any other filter settings. When this flag is specified, <b>NULL</b> must be passed for all other parameters. After setting this flag, the application can call <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> to retrieve the complete unfiltered list.

</td>
</tr>
</table>

### -param pwszLanguagesBuffer [in, optional]

Pointer to a double null-terminated multi-string buffer that contains an ordered, null-delimited list, in the format specified by <i>dwFlags</i>.

To clear the thread preferred UI languages list, an application sets this parameter to a null string or an empty double null-terminated string. 
If an application clears a language list, it should specify either a format flag or 0 for the <i>dwFlags</i> parameter.

When the application specifies one of the filtering flags, it must set this parameter to <b>NULL</b>. In this case, the function succeeds, but does not reset the thread preferred languages.

### -param pulNumLanguages [out, optional]

Pointer to the number of languages that the function has set in the thread preferred UI languages list. When the application specifies one of the filtering flags, the function must set this parameter to <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> otherwise.

## -remarks

When the application loads resources after a call to this function, the thread-specific preferences take priority over the languages preferred by the user.

This function can set up to five preferred languages for the thread, in order of preference. If the language buffer contains more than five valid languages, the function sets the first five valid languages and ignores the rest.

If the application calls this function with the MUI_LANGUAGE_ID flag set, the strings in the language list must use hexadecimal language 

identifiers that do not include the leading 0x, and are 4 characters in length. For example, en-US should be 

passed as "0409" and en as "0009".

When MUI_LANGUAGE_ID is specified, the hexadecimal values in the language list must each represent an actual language identifier. In particular, the following locale identifier values cannot be used to correspond to the language identifier: 

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
Calling this function with an empty language list and setting the MUI_CONSOLE_FILTER flag has the same effect as calling <a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a> with the language identifier set to 0. The language is set appropriately for use in a console window.

After this function returns, the application can call <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> to verify and examine the resulting language list. When MUI_CONSOLE_FILTER or MUI_COMPLEX_FILTER has been set by <b>SetThreadPreferredUILanguages</b>, the <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> function replaces with the fallback the languages the console cannot display using the current operating system language setting. The fallback for a language is determined based on the value of <a href="/windows/desktop/Intl/locale-sconsolefallbackname">LOCALE_SCONSOLEFALLBACKNAME</a> for the language.

Setting the MUI_COMPLEX_SCRIPT_FILTER flag in the call to <b>SetThreadPreferredUILanguages</b> causes <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a>  to remove languages that the console cannot display with languages that can only be rendered using <a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>, and insert the fallback language as the ultimate fallback. Examples of such languages are Arabic or the various Indic languages.

Setting the MUI_CONSOLE_FILTER flag in the call to <b>SetThreadPreferredUILanguages</b> causes <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> to remove languages the console cannot display with the current system setting and insert the fallback language as the ultimate fallback, because the console is limited to displaying characters from a single <a href="/windows/desktop/Intl/code-pages">code page</a>. For example, if the user language is Japanese (Japan), but the current console code page is the code page for Russian (Russia), the console displays Japanese-language text mostly as a series of character-not-found symbols. <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> chooses a language from the fallback list that will be legible in the console.

<div class="alert"><b>Note</b>  Resource-loading functions, such as <a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>, and <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>, also make calls to <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a>.</div>
<div> </div>
To change the code page, the application uses the <b>setlocale</b> function, or equivalent.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean SetThreadPreferredUILanguages(
            System.UInt32 dwFlags,
            System.String pwszLanguagesBuffer,
            ref System.UInt32 pulNumLanguages
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>