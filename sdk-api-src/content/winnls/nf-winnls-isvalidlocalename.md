---
UID: NF:winnls.IsValidLocaleName
title: IsValidLocaleName function (winnls.h)
description: Determines if the specified locale name is valid for a locale that is installed or supported on the operating system.Note  An application running only on Windows Vista and later should call this function in preference to IsValidLocale to determine the validity of a supplemental locale.
helpviewer_keywords: ["IsValidLocaleName","IsValidLocaleName function [Internationalization for Windows Applications]","_win32_IsValidLocaleName","intl.isvalidlocalename","winnls/IsValidLocaleName"]
old-location: intl\isvalidlocalename.htm
tech.root: Intl
ms.assetid: cd1b5a4e-7a9c-47a1-9ece-284fce3d5be4
ms.date: 12/05/2018
ms.keywords: IsValidLocaleName, IsValidLocaleName function [Internationalization for Windows Applications], _win32_IsValidLocaleName, intl.isvalidlocalename, winnls/IsValidLocaleName
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IsValidLocaleName
 - winnls/IsValidLocaleName
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
 - IsValidLocaleName
---

# IsValidLocaleName function


## -description

Determines if the specified <a href="/windows/desktop/Intl/locale-names">locale name</a> is valid for a locale that is installed or supported on the operating system.<div class="alert"><b>Note</b>  An application running only on Windows Vista and later should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-isvalidlocale">IsValidLocale</a> to determine the validity of a <a href="/windows/desktop/Intl/custom-locales">supplemental locale</a>.</div>
<div> </div>

## -parameters

### -param lpLocaleName [in]

Pointer to the locale name to validate.

## -returns

Returns a nonzero value if the locale name is valid, or returns 0 for an invalid name.

## -remarks

On Windows Vista and later, all supported locales should be installed on all operating systems.

This function can handle the name of a <a href="/windows/desktop/Intl/custom-locales">custom locale</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.


#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-isvalidlocale">IsValidLocale</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>