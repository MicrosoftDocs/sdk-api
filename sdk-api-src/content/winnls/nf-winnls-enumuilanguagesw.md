---
UID: NF:winnls.EnumUILanguagesW
title: EnumUILanguagesW function
author: windows-driver-content
description: Enumerates the user interface languages that are available on the operating system and calls the callback function with every language in the list.
old-location: intl\enumuilanguages.htm
old-project: Intl
ms.assetid: f97df853-fc40-4529-b8a5-27069863a9b9
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: EnumUILanguages, EnumUILanguages function [Internationalization for Windows Applications], EnumUILanguagesA, EnumUILanguagesW, MUI_ALL_INSTALLED_LANGUAGES, MUI_GROUP_POLICY, MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, MUI_LICENSED_LANGUAGES, _win32_EnumUILanguages, intl.enumuilanguages, winnls/EnumUILanguages, winnls/EnumUILanguagesA, winnls/EnumUILanguagesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumUILanguagesW (Unicode) and EnumUILanguagesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	EnumUILanguages
-	EnumUILanguagesA
-	EnumUILanguagesW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumUILanguagesW function


## -description


Enumerates the user interface languages that are available on the operating system and calls the callback function with every language in the list.


## -parameters




### -param lpUILanguageEnumProc [in]

Pointer to an application-defined <a href="https://msdn.microsoft.com/5890bde9-7089-4440-a9cf-04b502183770">EnumUILanguagesProc</a> callback function. <b>EnumUILanguages</b> calls this function repeatedly to enumerate the languages in the list.


### -param dwFlags [in]

Flags identifying language format and filtering. The following flags specify the format of the language to pass to the callback function. The format flags are mutually exclusive, and MUI_LANGUAGE_ID is the default. 

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
Pass the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> in the language string to the callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Pass the <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> in the language string to the callback function.

</td>
</tr>
</table>
 

The following flags specify the filtering for the function to use in enumerating the languages. The filtering flags are mutually exclusive, and the default is MUI_LICENSED_LANGUAGES.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_ALL_INSTALLED_LANGUAGES"></a><a id="mui_all_installed_languages"></a><dl>
<dt><b>MUI_ALL_INSTALLED_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all installed languages available to the operating system.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LICENSED_LANGUAGES"></a><a id="mui_licensed_languages"></a><dl>
<dt><b>MUI_LICENSED_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all installed languages that are available and licensed for use.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_GROUP_POLICY"></a><a id="mui_group_policy"></a><dl>
<dt><b>MUI_GROUP_POLICY</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all installed languages that are available and licensed, and that are allowed by 

the group policy.

</td>
</tr>
</table>
 

<b>Windows Vista and later:</b> The application can set <i>dwFlags</i> to 0, or to one or more of the specified flags. A setting of 0 causes the parameter value to default to MUI_LANGUAGE_ID | MUI_LICENSED_LANGUAGES.

<b>Windows 2000, Windows XP, Windows Server 2003:</b> The application must set <i>dwFlags</i> to 0.


### -param lParam [in]

Application-defined value.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates the user interface languages that are available and, depending on the flag specified, licensed for use on the operating system. It passes language identifiers or language names, one at a time, to the <a href="https://msdn.microsoft.com/5890bde9-7089-4440-a9cf-04b502183770">EnumUILanguagesProc</a> callback function. The <b>EnumUILanguages</b> function continues to pass language identifiers or names to the callback function until the last language is found or the callback function returns <b>FALSE</b>.

For applications that run only on Windows Vista and later, MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID. MUI_LANGUAGE_NAME allows differentiation between languages that are associated with a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">supplemental locale</a>.

If the MUI_LANGUAGE_ID flag is specified in the call to this function, the strings passed to the callback 

function will be hexadecimal language identifiers that do not include the leading 0x, and will be 4 

characters in length. For example, en-US will be passed as "0409" and en as "0009". The value "1000" is passed to the callback function for any language associated with a supplemental locale. This value corresponds to the hexadecimal value of <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>. It does not distinguish among supplemental locales, even if the selected language is in the user preferred UI languages list or the system preferred UI languages list.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean EnumUILanguages(
            EnumUILanguagesProc lpUILanguageEnumProc,
            System.UInt32 dwFlags,
            System.IntPtr lParam
            );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5890bde9-7089-4440-a9cf-04b502183770">EnumUILanguagesProc</a>



<a href="https://msdn.microsoft.com/34fc125d-0f0b-43d0-aa2b-91501bd6cd26">GetSystemDefaultUILanguage</a>



<a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

