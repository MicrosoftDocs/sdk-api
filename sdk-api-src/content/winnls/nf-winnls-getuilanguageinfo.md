---
UID: NF:winnls.GetUILanguageInfo
title: GetUILanguageInfo function
author: windows-sdk-content
description: Retrieves a variety of information about an installed UI language:
old-location: intl\getuilanguageinfo.htm
old-project: Intl
ms.assetid: 7eb17073-f79a-4a87-a85b-94007e77888a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetUILanguageInfo, GetUILanguageInfo function [Internationalization for Windows Applications], MUI_FULL_LANGUAGE, MUI_LANGUAGE_ID, MUI_LANGUAGE_INSTALLED, MUI_LANGUAGE_LICENSED, MUI_LANGUAGE_NAME, MUI_LIP_LANGUAGE, MUI_PARTIAL_LANGUAGE, _win32_GetUILanguageInfo, intl.getuilanguageinfo, winnls/GetUILanguageInfo
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUILanguageInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUILanguageInfo function


## -description


Retrieves a variety of information about an installed UI language:
<ul>
<li>Is the language installed?</li>
<li>Is the current user licensed to use the language?</li>
<li>Is the language fully localized? Partially localized? Part of a Language Installation Pack (LIP)?</li>
<li>If it is partially localized or part of an LIP:<ul>
<li>What is its fallback language?  </li>
<li>If that fallback language is a partially localized language, what is its base?</li>
<li>What is the default fallback language?</li>
</ul>
</li>
</ul>

## -parameters




### -param dwFlags [in]

Flags defining the format of the specified language. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

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
Retrieve the language strings in <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language strings in <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> format.

</td>
</tr>
</table>
 


### -param pwmszLanguage [in]

Pointer to languages for which the function is to retrieve information. This parameter indicates an ordered, null-delimited list of language identifiers or language names, depending on the flag setting. For information on the use of this parameter, see the Remarks section.


### -param pwszFallbackLanguages [out, optional]

Pointer to a buffer in which this function retrieves an ordered, null-delimited list of fallback languages, formatted as defined by the setting for <i>dwFlags</i>. This list ends with two null characters.

Alternatively if this parameter is set to <b>NULL</b> and <i>pcchLanguagesBuffer</i> is set to 0, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. The required size includes the two null characters.


### -param pcchFallbackLanguages [in, out, optional]

Pointer to the size, in characters, for the language buffer indicated by <i>pwszFallbackLanguages</i>. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and <i>pwszLanguagesBuffer </i>is set to <b>NULL</b>, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>.


### -param pAttributes

TBD




#### - pdwAttributes [out]

Pointer to flags indicating attributes of the input language list. The function always retrieves the flag characterizing the last language listed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_FULL_LANGUAGE"></a><a id="mui_full_language"></a><dl>
<dt><b>MUI_FULL_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
The language is fully localized.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_PARTIAL_LANGUAGE"></a><a id="mui_partial_language"></a><dl>
<dt><b>MUI_PARTIAL_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
The language is partially localized.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LIP_LANGUAGE"></a><a id="mui_lip_language"></a><dl>
<dt><b>MUI_LIP_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
The language is an LIP language.

</td>
</tr>
</table>
 

In addition, <i>pdwAttributes</i> includes one or both of the following flags, as appropriate.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_INSTALLED"></a><a id="mui_language_installed"></a><dl>
<dt><b>MUI_LANGUAGE_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The language is installed on this computer.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_LICENSED"></a><a id="mui_language_licensed"></a><dl>
<dt><b>MUI_LANGUAGE_LICENSED</b></dt>
</dl>
</td>
<td width="60%">
The language is appropriately licensed for the current user.

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid. For more information, see Remarks.</li>
<li>ERROR_OBJECT_NAME_NOT_FOUND. The specified object name was not found, or it was not valid, or the first language in the input list is not an installed language. For more information, see Remarks.
</li>
</ul>
If <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns any other error code, the parameters <i>pcchFallbackLanguages</i> and <i>pdwAttributes</i> are undefined.




## -remarks



MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID because it allows the function to do a better job of handling LIP languages that do not correspond to predefined locales, but instead correspond to a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>. LIP languages that correspond to predefined locales are handled just like non-LIP languages.

If the MUI_LANGUAGE_ID flag is specified, the supplied language strings must 

use hexadecimal language identifiers that do not include the leading 0x, and are 4 characters in length. 

For example, en-US should be passed as "0409" and en as "0009". The returned language strings will be in the 

same format.

When MUI_LANGUAGE_ID is specified, and if there is such a language in the user preferred UI languages list, there can be only one such language in the list. That language can be specified in <i>pwmszLanguage</i> as "1400", which corresponds to the hexadecimal value of <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>. No other such language can be specified using MUI_LANGUAGE_ID. Using "1000", which corresponds to the hexadecimal value of <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>, in the string indicated by <i>pwmszLanguage</i> will result in an ERROR_INVALID_PARAMETER code.

A partially localized language can have a fallback language that is partially localized, requiring repeated calls to <b>GetUILanguageInfo</b> to obtain full information. Consider the case of a partially localized language Lang1 that offers a choice of three fallback languages. The Lang3 fallback language is partially localized, and offers a choice of two fallback languages. The dependencies are as follows, with the default fallback listed first:

<ul>
<li>Lang1<ul>
<li>Lang2</li>
<li>Lang3<ul>
<li>Lang5</li>
<li>Lang6</li>
</ul>
</li>
<li>Lang4</li>
</ul>
</li>
</ul>
To get the fallback language(s) of Lang1, the application passes in <i>pwmszLanguage</i> as "Lang1\0\0". On return from the function, <i>pwszFallbackLanguages</i> is set to "Lang2\0Lang3\0Lang4\0\0". Note that the ordering of this list indicates that Lang2 is the default fallback language.

To get the fallback language(s) of Lang3 in relation to Lang1, the application passes in <i>pwmszLanguage</i> as "lang1\0\lang3\0\0". On return from the function, <i>pwszFallbackLanguages</i> is set to "Lang5\0Lang6\0\0".

This function returns ERROR_INVALID_PARAMETER for any of the following:

<ul>
<li><i>pwmszLanguage</i> is <b>NULL</b> or empty.</li>
<li>Both MUI_LANGUAGE_ID and MUI_LANGUAGE_NAME are set.</li>
<li>Any flags other than MUI_LANGUAGE_ID or MUI_LANGUAGE_NAME are set.</li>
<li><i>pcchFallbackLanguages</i> is greater than 0 but <i>pwszFallbackLanguages</i> is <b>NULL</b>.</li>
<li><i>pwmszLanguage</i> cannot be parsed as a multi-string buffer of language identifiers or language names, depending on the flag setting.</li>
</ul>
The ERROR_OBJECT_NAME_NOT_FOUND error code occurs if <i>pwmszLanguage</i> can be parsed, but is not valid. The code might also be returned for an invalid locale identifier, or if the first language in the input list is not an installed language, or if a fully localized language has defined a fallback language.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetUILanguageInfo(
            System.UInt32 dwFlags,
            System.String pwmszLanguage,
            System.IntPtr pwszFallbackLanguages,
            ref System.UInt32 pcchFallbackLanguages,
            ref System.UInt32 pdwAttributes
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f97df853-fc40-4529-b8a5-27069863a9b9">EnumUILanguages</a>



<a href="https://msdn.microsoft.com/df1eee13-012a-47e6-a6de-8ddb8ecc6036">GetFileMUIInfo</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

