---
UID: NF:winnls.SetThreadPreferredUILanguages
title: SetThreadPreferredUILanguages function
author: windows-sdk-content
description: Sets the thread preferred UI languages for the current thread. For more information, see User Interface Language Management.
old-location: intl\setthreadpreferreduilanguages.htm
old-project: Intl
ms.assetid: 32a8117c-2cb2-4559-8e86-9fad5b28aa5b
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: MUI_COMPLEX_SCRIPT_FILTER, MUI_CONSOLE_FILTER, MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, MUI_RESET_FILTERS, SetThreadPreferredUILanguages, SetThreadPreferredUILanguages function [Internationalization for Windows Applications], _win32_SetThreadPreferredUILanguages, intl.setthreadpreferreduilanguages, winnls/SetThreadPreferredUILanguages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetThreadPreferredUILanguages
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetThreadPreferredUILanguages function


## -description


Sets the thread preferred UI languages for the current thread. For more information, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.


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
The input parameter language strings are in <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The input parameter language strings are in <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> format.

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

<a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> should replace with the appropriate fallback all languages having <a href="uniscribe_glossary.htm">complex scripts</a>. When this flag is specified, <b>NULL</b> must be passed for all other parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_CONSOLE_FILTER"></a><a id="mui_console_filter"></a><dl>
<dt><b>MUI_CONSOLE_FILTER</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> should replace with the appropriate fallback all languages that cannot display properly in a console window with the current operating system settings. When this flag is specified, <b>NULL</b> must be passed for all other parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_RESET_FILTERS"></a><a id="mui_reset_filters"></a><dl>
<dt><b>MUI_RESET_FILTERS</b></dt>
</dl>
</td>
<td width="60%">
Reset the filtering for the language list by removing any other filter settings. When this flag is specified, <b>NULL</b> must be passed for all other parameters. After setting this flag, the application can call <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> to retrieve the complete unfiltered list.

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
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>
Calling this function with an empty language list and setting the MUI_CONSOLE_FILTER flag has the same effect as calling <a href="https://msdn.microsoft.com/30a0cecf-0ed1-4c03-bd5e-da07b1828c75">SetThreadUILanguage</a> with the language identifier set to 0. The language is set appropriately for use in a console window.

After this function returns, the application can call <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> to verify and examine the resulting language list. When MUI_CONSOLE_FILTER or MUI_COMPLEX_FILTER has been set by <b>SetThreadPreferredUILanguages</b>, the <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> function replaces with the fallback the languages the console cannot display using the current operating system language setting. The fallback for a language is determined based on the value of <a href="https://msdn.microsoft.com/36465a1c-085f-4f80-ad3d-5be6eaefe943">LOCALE_SCONSOLEFALLBACKNAME</a> for the language.

Setting the MUI_COMPLEX_SCRIPT_FILTER flag in the call to <b>SetThreadPreferredUILanguages</b> causes <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a>  to remove languages that the console cannot display with languages that can only be rendered using <a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>, and insert the fallback language as the ultimate fallback. Examples of such languages are Arabic or the various Indic languages.

Setting the MUI_CONSOLE_FILTER flag in the call to <b>SetThreadPreferredUILanguages</b> causes <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> to remove languages the console cannot display with the current system setting and insert the fallback language as the ultimate fallback, because the console is limited to displaying characters from a single <a href="https://msdn.microsoft.com/866f09f4-629e-4097-a974-fbda9389d077">code page</a>. For example, if the user language is Japanese (Japan), but the current console code page is the code page for Russian (Russia), the console displays Japanese-language text mostly as a series of character-not-found symbols. <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a> chooses a language from the fallback list that will be legible in the console.

<div class="alert"><b>Note</b>  Resource-loading functions, such as <a href="_win32_LoadString_cpp">LoadString</a>, <a href="_win32_LoadImage_cpp">LoadImage</a>, and <a href="_win32_FindResource_cpp">FindResource</a>, also make calls to <a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a>.</div>
<div> </div>
To change the code page, the application uses the <b>setlocale</b> function, or equivalent.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean SetThreadPreferredUILanguages(
            System.UInt32 dwFlags,
            System.String pwszLanguagesBuffer,
            ref System.UInt32 pulNumLanguages
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8501b8b3-c8bf-4bef-b65f-6c0f455f0c7d">GetThreadPreferredUILanguages</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>



<a href="https://msdn.microsoft.com/30a0cecf-0ed1-4c03-bd5e-da07b1828c75">SetThreadUILanguage</a>
 

 

