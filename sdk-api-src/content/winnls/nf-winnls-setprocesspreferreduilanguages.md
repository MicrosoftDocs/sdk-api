---
UID: NF:winnls.SetProcessPreferredUILanguages
title: SetProcessPreferredUILanguages function (winnls.h)
description: Sets the process preferred UI languages for the application process. For more information, see User Interface Language Management.
helpviewer_keywords: ["MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","SetProcessPreferredUILanguages","SetProcessPreferredUILanguages function [Internationalization for Windows Applications]","intl.setprocesspreferreduilanguages","winnls/SetProcessPreferredUILanguages"]
old-location: intl\setprocesspreferreduilanguages.htm
tech.root: Intl
ms.assetid: 81f65561-886d-4c29-aca6-ea69bc865ea0
ms.date: 12/05/2018
ms.keywords: MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, SetProcessPreferredUILanguages, SetProcessPreferredUILanguages function [Internationalization for Windows Applications], intl.setprocesspreferreduilanguages, winnls/SetProcessPreferredUILanguages
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
 - SetProcessPreferredUILanguages
 - winnls/SetProcessPreferredUILanguages
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
 - SetProcessPreferredUILanguages
---

# SetProcessPreferredUILanguages function


## -description

Sets the process preferred UI languages for the application process. For more information, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.

## -parameters

### -param dwFlags [in]

Flags identifying the language format to use for the process preferred UI languages. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME. 

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

### -param pwszLanguagesBuffer [in, optional]

Pointer to a double null-terminated multi-string buffer that contains an ordered, null-delimited list in decreasing order of preference. If there are more than five languages in the buffer, the function only sets the first five valid languages.

Alternatively, this parameter can contain <b>NULL</b> if no language list is required. In this case, the function clears the preferred UI languages for the process.

### -param pulNumLanguages [out, optional]

Pointer to the number of languages that has been set in the process language list from the input buffer, up to a maximum of five.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return the following error code:

<ul>
<li>ERROR_INVALID_PARAMETER. An invalid parameter is specified.</li>
</ul>
If the process preferred UI languages list is empty or if the languages specified for the process are not valid, the function succeeds and sets 0 in the <i>pulNumLanguages</i> parameter.

## -remarks

Ideally, applications will call <b>SetProcessPreferredUILanguages</b> as soon as possible after launching.

After this function returns, the application can call <a href="/windows/desktop/api/winnls/nf-winnls-getprocesspreferreduilanguages">GetProcessPreferredUILanguages</a> to verify and examine the resulting language list.

When MUI_LANGUAGE_ID is specified, the input parameter language strings must use hexadecimal language 

identifiers that do not include the leading 0x, and are 4 characters in length. For example, en-US should be 

passed as "0409" and en as "0009".

<div class="alert"><b>Note</b>  Use of MUI_LANGUAGE_NAME is recommended over MUI_LANGUAGE_ID.</div>
<div> </div>
<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean SetProcessPreferredUILanguages(
            System.UInt32 dwFlags,
            System.String pwszLanguagesBuffer,
            ref System.UInt32 pulNumLanguages
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getprocesspreferreduilanguages">GetProcessPreferredUILanguages</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>