---
UID: NF:winnls.GetNLSVersion
title: GetNLSVersion function (winnls.h)
description: Retrieves information about the current version of a specified NLS capability for a locale specified by identifier.Note  For interoperability reasons, the application should prefer the GetNLSVersionEx function to GetNLSVersion because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, for which GetNLSVersionEx retrieves enough information to determine if sort behavior has changed. Any application that runs only on Windows Vista and later should use GetNLSVersionEx or at least pass the NLSVERSIONINFOEX structure when calling GetNLSVersion to obtain additional sorting versioning data.
helpviewer_keywords: ["GetNLSVersion","GetNLSVersion function [Internationalization for Windows Applications]","_win32_GetNLSVersion","intl.getnlsversion","winnls/GetNLSVersion"]
old-location: intl\getnlsversion.htm
tech.root: Intl
ms.assetid: 09bc53e1-69f4-4a71-82b3-1b1b84a1b84f
ms.date: 12/05/2018
ms.keywords: GetNLSVersion, GetNLSVersion function [Internationalization for Windows Applications], _win32_GetNLSVersion, intl.getnlsversion, winnls/GetNLSVersion
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
 - GetNLSVersion
 - winnls/GetNLSVersion
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
 - GetNLSVersion
---

# GetNLSVersion function


## -description

Retrieves information about the current version of a specified NLS capability for a locale specified by identifier.<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a> function to <b>GetNLSVersion</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, for which <b>GetNLSVersionEx</b> retrieves enough information to determine if sort behavior has changed. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a> or at least pass the <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure when calling <b>GetNLSVersion</b> to obtain additional sorting versioning data.</div>
<div> </div>

## -parameters

### -param Function [in]

The NLS capability to query. This value must be COMPARE_STRING. See the <a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a> enumeration.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
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

### -param lpVersionInformation [in, out]

Pointer to an <a href="/windows/win32/api/winnls/ns-winnls-nlsversioninfo-r1">NLSVERSIONINFO</a> structure. The application must initialize the <b>dwNLSVersionInfoSize</b> member to <code>sizeof(NLSVERSIONINFO)</code>.

<div class="alert"><b>Note</b>  On Windows Vista and later, the function can alternatively provide version information in an <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure.</div>
<div> </div>

## -returns

Returns <b>TRUE</b> if and only if the application has supplied valid values in <i>lpVersionInformation</i>, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table. If it does not, there is no need to re-index the table. For more information, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/win32/api/winnls/ns-winnls-nlsversioninfo-r1">NLSVERSIONINFO</a>



<a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a>