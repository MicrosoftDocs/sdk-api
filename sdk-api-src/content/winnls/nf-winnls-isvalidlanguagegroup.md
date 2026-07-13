---
UID: NF:winnls.IsValidLanguageGroup
title: IsValidLanguageGroup function (winnls.h)
description: Determines if a language group is installed or supported on the operating system. For more information, see NLS Terminology.
helpviewer_keywords: ["IsValidLanguageGroup","IsValidLanguageGroup function [Internationalization for Windows Applications]","LGRPID_INSTALLED","LGRPID_SUPPORTED","_win32_IsValidLanguageGroup","intl.isvalidlanguagegroup","winnls/IsValidLanguageGroup"]
old-location: intl\isvalidlanguagegroup.htm
tech.root: Intl
ms.assetid: 68cf09f8-fe97-4035-94b6-886ca26bbf3e
ms.date: 12/05/2018
ms.keywords: IsValidLanguageGroup, IsValidLanguageGroup function [Internationalization for Windows Applications], LGRPID_INSTALLED, LGRPID_SUPPORTED, _win32_IsValidLanguageGroup, intl.isvalidlanguagegroup, winnls/IsValidLanguageGroup
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IsValidLanguageGroup
 - winnls/IsValidLanguageGroup
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
 - IsValidLanguageGroup
---

# IsValidLanguageGroup function


## -description

Determines if a language group is installed or supported on the operating system. For more information, see <a href="/windows/desktop/Intl/nls-terminology">NLS Terminology</a>.

## -parameters

### -param LanguageGroup [in]

Identifier of language group to validate. This parameter can have one of the following values:

<ul>
<li>LGRPID_ARABIC</li>
<li>LGRPID_ARMENIAN
</li>
<li>LGRPID_BALTIC</li>
<li>LGRPID_CENTRAL_EUROPE</li>
<li>LGRPID_CYRILLIC</li>
<li>LGRPID_GEORGIAN
</li>
<li>LGRPID_GREEK</li>
<li>LGRPID_HEBREW</li>
<li>LGRPID_INDIC</li>
<li>LGRPID_JAPANESE</li>
<li>LGRPID_KOREAN
</li>
<li>LGRPID_SIMPLIFIED_CHINESE</li>
<li>LGRPID_TRADITIONAL_CHINESE</li>
<li>LGRPID_THAI</li>
<li>LGRPID_TURKIC</li>
<li>LGRPID_TURKISH
</li>
<li>LGRPID_VIETNAMESE</li>
<li>LGRPID_WESTERN_EUROPE</li>
</ul>

### -param dwFlags [in]

Flag specifying the validity test to apply to the language group identifier. This parameter can be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LGRPID_INSTALLED"></a><a id="lgrpid_installed"></a><dl>
<dt><b>LGRPID_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Determine if language group identifier is both supported and installed.

</td>
</tr>
<tr>
<td width="40%"><a id="LGRPID_SUPPORTED"></a><a id="lgrpid_supported"></a><dl>
<dt><b>LGRPID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Determine if language group identifier is supported.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if the language group identifier passes the specified validity test, or <b>FALSE</b> otherwise.

## -remarks

If the LGRPID_INSTALLED flag is specified and this function returns <b>TRUE</b>, the language group identifier is both supported and installed on the operating system.

If the LGRPID_SUPPORTED flag is specified and this function returns <b>TRUE</b>, the language group identifier is supported in the release, but not necessarily installed on the operating system.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlanguagegroupsa">EnumSystemLanguageGroups</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>