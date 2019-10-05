---
UID: NF:winnls.GetUserPreferredUILanguages
title: GetUserPreferredUILanguages function (winnls.h)
author: windows-sdk-content
description: Retrieves information about the user preferred UI languages. For more information, see User Interface Language Management.
old-location: intl\getuserpreferreduilanguages.htm
tech.root: Intl
ms.assetid: 0800642c-c133-4993-bd16-6bdbf7518f1c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserPreferredUILanguages, GetUserPreferredUILanguages function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, _win32_GetUserPreferredUILanguages, intl.getuserpreferreduilanguages, winnls/GetUserPreferredUILanguages
ms.topic: function
f1_keywords: 
 - "winnls/GetUserPreferredUILanguages"
dev_langs:
 - c++
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
 - GetUserPreferredUILanguages
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUserPreferredUILanguages function


## -description


Retrieves information about the user preferred UI languages. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.


## -parameters




### -param dwFlags [in]

Flags identifying language format and filtering. The following flags specify the language format to use for the user preferred UI languages list. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

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
Retrieve the language strings in <a href="https://docs.microsoft.com/windows/desktop/Intl/language-identifiers">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language strings in <a href="https://docs.microsoft.com/windows/desktop/Intl/language-names">language name</a> format.

</td>
</tr>
</table>
 


### -param pulNumLanguages [out]

Pointer to the number of languages retrieved in <i>pwszLanguagesBuffer</i>.


### -param pwszLanguagesBuffer [out, optional]

Optional. Pointer to a buffer in which this function retrieves an ordered, null-delimited user preferred UI languages list, in the format specified by <i>dwflags</i>. This list ends with two null characters.

Alternatively if this parameter is set to <b>NULL</b> and <i>pcchLanguagesBuffer</i> is set to 0, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. The required size includes the two null characters.


### -param pcchLanguagesBuffer [in, out]

Pointer to the size, in characters, for the language buffer indicated by <i>pwszLanguagesBuffer</i>. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and <i>pwszLanguagesBuffer</i> is set to <b>NULL</b>, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. 


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes: 
<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>


If the function fails for any other reason, the values of <i>pulNumLanguages</i> and <i>pcchLanguagesBuffer</i> are undefined.




## -remarks



When MUI_LANGUAGE_ID is specified, the language strings retrieved will be hexadecimal language identifiers 

that do not include the leading 0x, and will be 4 characters in length. For example, en-US will be returned 

as "0409" and en as "0009".

The user preferred UI languages cannot include more than one Language Interface Pack (LIP) language that corresponds to a <a href="https://docs.microsoft.com/windows/desktop/Intl/custom-locales">supplemental locale</a>. If the list includes more than one of these languages, and if the application specifies MUI_LANGUAGE_ID in the call to the function, the language buffer contains "1400" for that language. This string corresponds to the hexadecimal value of <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>.

The language list retrieved by this function has the following characteristics:

<ul>
<li>Each language represents a valid NLS locale.</li>
<li>Each language is installed on the operating system.</li>
<li>The list contains one entry for each language, with no duplicate entries.</li>
<li>If the list is empty or does not meet these validation criteria, the system preferred UI languages list is used instead.</li>
</ul>
<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetUserPreferredUILanguages(
            System.UInt32 dwFlags,
            ref System.UInt32 pulNumLanguages,
            System.IntPtr pwszLanguagesBuffer,
            ref System.UInt32 pcchLanguagesBuffer
            );

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getsystempreferreduilanguages">GetSystemPreferredUILanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getthreaduilanguage">GetThreadUILanguage</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>
 

 

