---
UID: NF:winnls.EnumSystemLanguageGroupsA
title: EnumSystemLanguageGroupsA function (winnls.h)
description: Enumerates the language groups that are either installed on or supported by an operating system. (ANSI)
helpviewer_keywords: ["EnumSystemLanguageGroupsA", "LGRPID_INSTALLED", "LGRPID_SUPPORTED", "winnls/EnumSystemLanguageGroupsA"]
old-location: intl\enumsystemlanguagegroups.htm
tech.root: Intl
ms.assetid: 8cc2335e-b222-44d9-a966-4b6803639071
ms.date: 12/05/2018
ms.keywords: EnumSystemLanguageGroups, EnumSystemLanguageGroups function [Internationalization for Windows Applications], EnumSystemLanguageGroupsA, EnumSystemLanguageGroupsW, LGRPID_INSTALLED, LGRPID_SUPPORTED, _win32_EnumSystemLanguageGroups, intl.enumsystemlanguagegroups, winnls/EnumSystemLanguageGroups, winnls/EnumSystemLanguageGroupsA, winnls/EnumSystemLanguageGroupsW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumSystemLanguageGroupsW (Unicode) and EnumSystemLanguageGroupsA (ANSI)
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
 - EnumSystemLanguageGroupsA
 - winnls/EnumSystemLanguageGroupsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumSystemLanguageGroups
 - EnumSystemLanguageGroupsA
 - EnumSystemLanguageGroupsW
---

# EnumSystemLanguageGroupsA function


## -description

Enumerates the language groups that are either installed on or supported by an operating system. <div class="alert"><b>Note</b>  For custom locales, your application should call <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> instead of <b>EnumSystemLanguageGroups</b>.</div>
<div> </div>

## -parameters

### -param lpLanguageGroupEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317821(v=vs.85)">EnumLanguageGroupsProc</a>.

### -param dwFlags [in]

Flags specifying the language group identifiers to enumerate. This parameter can have one of the following values.

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
Enumerate only installed language group identifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="LGRPID_SUPPORTED"></a><a id="lgrpid_supported"></a><dl>
<dt><b>LGRPID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all supported language group identifiers.

</td>
</tr>
</table>

### -param lParam [in]

Application-defined value to pass to the callback function. This parameter can be used in error checking. It can also be used to ensure thread safety in the callback function.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates language groups by passing language group identifiers, one at a time, to the specified application-defined callback function. This process continues until the last language group identifier is found or the callback function returns <b>FALSE</b>.





> [!NOTE]
> The winnls.h header defines EnumSystemLanguageGroups as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a>



<a href="/previous-versions/windows/desktop/legacy/dd317821(v=vs.85)">EnumLanguageGroupsProc</a>



<a href="/windows/desktop/api/winnls/nf-winnls-isvalidlanguagegroup">IsValidLanguageGroup</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
