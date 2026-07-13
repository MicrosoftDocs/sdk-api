---
UID: NF:winnls.LocaleNameToLCID
title: LocaleNameToLCID function (winnls.h)
description: Converts a locale name to a locale identifier.
helpviewer_keywords: ["LocaleNameToLCID","LocaleNameToLCID function [Internationalization for Windows Applications]","_win32_LocaleNameToLCID","intl.localenametolcid","winnls/LocaleNameToLCID"]
old-location: intl\localenametolcid.htm
tech.root: Intl
ms.assetid: 00404566-b9ef-43ea-8056-ca9ab0117814
ms.date: 12/05/2018
ms.keywords: LocaleNameToLCID, LocaleNameToLCID function [Internationalization for Windows Applications], _win32_LocaleNameToLCID, intl.localenametolcid, winnls/LocaleNameToLCID
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
 - LocaleNameToLCID
 - winnls/LocaleNameToLCID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - api-ms-win-core-localization-l1-2-3.dll
api_name:
 - LocaleNameToLCID
---

# LocaleNameToLCID function


## -description

Converts a [locale name](/windows/desktop/Intl/locale-names) to a [locale identifier](/windows/desktop/Intl/locale-identifiers).

## -parameters

### -param lpName [in]

Pointer to a null-terminated string representing a locale name, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

<b>Prior to Windows 7:</b>Reserved; should always be 0.

<b>Beginning in Windows 7:</b> Can be set to <a href="/windows/desktop/Intl/locale-allow-neutral-names">LOCALE_ALLOW_NEUTRAL_NAMES</a> to allow the return of a neutral LCID.

## -returns

If successful, returns the locale identifier corresponding to the locale name.

If the supplied locale name corresponds to a custom locale that is the user default, this function returns <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>.

If the locale name corresponds to a custom locale that is not the user default, is a transient locale, or is a CLDR (Unicode Common Locale Data Repository) locale, the function returns <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return ERROR_INVALID_PARAMETER if any of the parameter values are invalid.
</ul>

## -remarks

For custom locales, including those created by Microsoft, your applications should prefer locale names over locale identifiers. See [The deprecation of LCIDs](/globalization/locale/locale-names#the-deprecation-of-lcids) for more info.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.


#### Examples


```cpp

#include "stdafx.h"
#include "windows.h"
#include "stdio.h"

int _cdecl main(
    int argc,
    char *argv[])
{
    WCHAR strNameBuffer[LOCALE_NAME_MAX_LENGTH];
    DWORD error = ERROR_SUCCESS;
    LCID  lcid;

    // Get the name for locale 0x10407 (German (German), with phonebook sort)
    if (LCIDToLocaleName(0x10407, strNameBuffer, LOCALE_NAME_MAX_LENGTH, 0) == 0)
    {
        // There was an error
        error = GetLastError();
    }
    else
    {
        // Success, display the locale name we found
        wprintf(L"Locale Name for 0x10407 is %s\n", strNameBuffer);
    }

    // Get the LCID for the locale
    lcid = LocaleNameToLCID(strNameBuffer, 0);
    if (lcid == 0)
    {
        // There was an error
        error = GetLastError();
    }
    else
    {
        // Success, print the round trip LCID
        wprintf(L"LCID for %s is 0x%x\n", strNameBuffer, lcid);
    }
}

/* This code example produces the following output:

Locale Name for 0x10407 is de-DE_phoneb
LCID for de-DE_phoneb is 0x10407

*/


```

## -see-also

<a href="/windows/desktop/Intl/downlevellocalenametolcid">DownlevelLocaleNameToLCID</a>



<a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
