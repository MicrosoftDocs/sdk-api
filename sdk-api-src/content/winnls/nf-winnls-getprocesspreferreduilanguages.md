---
UID: NF:winnls.GetProcessPreferredUILanguages
title: GetProcessPreferredUILanguages function (winnls.h)
description: Retrieves the process preferred UI languages. For more information, see User Interface Language Management.
helpviewer_keywords: ["GetProcessPreferredUILanguages","GetProcessPreferredUILanguages function [Internationalization for Windows Applications]","MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","intl.getprocesspreferreduilanguages","winnls/GetProcessPreferredUILanguages"]
old-location: intl\getprocesspreferreduilanguages.htm
tech.root: Intl
ms.assetid: 115fd1f4-39ae-4c69-aa42-606617a989aa
ms.date: 12/05/2018
ms.keywords: GetProcessPreferredUILanguages, GetProcessPreferredUILanguages function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, intl.getprocesspreferreduilanguages, winnls/GetProcessPreferredUILanguages
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetProcessPreferredUILanguages
 - winnls/GetProcessPreferredUILanguages
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
 - GetProcessPreferredUILanguages
---

# GetProcessPreferredUILanguages function


## -description

Retrieves the process preferred UI languages. For more information, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.

## -parameters

### -param dwFlags [in]

Flags identifying the language format to use for the process preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME. 

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

### -param pulNumLanguages [out]

Pointer to the number of languages retrieved in <i>pwszLanguagesBuffer</i>.

### -param pwszLanguagesBuffer [out, optional]

Optional. Pointer to a double null-terminated multi-string buffer in which the function retrieves an ordered, null-delimited list in preference order, starting with the most preferable. 

Alternatively if this parameter is set to <b>NULL</b> and <i>pcchLanguagesBuffer</i> is set to 0, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>. The required size includes the two null characters.

### -param pcchLanguagesBuffer [in, out]

Pointer to the size, in characters, for the language buffer indicated by <i>pwszLanguagesBuffer</i>. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and <i>pwszLanguagesBuffer</i> is set to <b>NULL</b>, the function retrieves the required size of the language buffer in <i>pcchLanguagesBuffer</i>.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>
If the process preferred UI language list is empty or if the languages specified for the process are not valid, the function succeeds and returns an empty multistring in <i>pwszLanguagesBuffer</i> and 2 in the <i>pcchLanguagesBuffer</i> parameter.

## -remarks

Depending on the flags specified by the application, this function can retrieve a list consisting of the process preferred UI languages. If it encounters a duplicate language, the function only retrieves the first instance of the duplicated language.

When MUI_LANGUAGE_ID is specified, the language strings retrieved will be hexadecimal language identifiers 

that do not include the leading 0x, and will be 4 characters in length. For example, en-US will be returned 

as "0409" and en as "0009".

<div class="alert"><b>Note</b>  Use of MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID.</div>
<div> </div>
<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetProcessPreferredUILanguages(
            System.UInt32 dwFlags,
            ref System.UInt32 pulNumLanguages,
            System.IntPtr pwszLanguagesBuffer,
            ref System.UInt32 pcchLanguagesBuffer
            );

```

## -see-also

<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setprocesspreferreduilanguages">SetProcessPreferredUILanguages</a>