---
UID: NF:winnls.LocaleNameToLCID
title: LocaleNameToLCID function
author: windows-sdk-content
description: Converts a locale name to a locale identifier.
old-location: intl\localenametolcid.htm
tech.root: Intl
ms.assetid: 00404566-b9ef-43ea-8056-ca9ab0117814
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: LocaleNameToLCID, LocaleNameToLCID function [Internationalization for Windows Applications], _win32_LocaleNameToLCID, intl.localenametolcid, winnls/LocaleNameToLCID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - LocaleNameToLCID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LocaleNameToLCID function


## -description


Converts a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a> to a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a>. <div class="alert"><b>Note</b>  For custom locales, including those created by Microsoft, your applications should prefer locale names over locale identifiers.</div>
<div> </div>



## -parameters




### -param lpName [in]

Pointer to a null-terminated string representing a locale name, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

<b>Prior to Windows 7:</b>Reserved; should always be 0.

<b>Beginning in Windows 7:</b> Can be set to <a href="https://msdn.microsoft.com/b4f9d07c-3c39-46aa-933d-5c8c6ae98345">LOCALE_ALLOW_NEUTRAL_NAMES</a> to allow the return of a neutral LCID.


## -returns



Returns the locale identifier corresponding to the locale name if successful. If the supplied locale name corresponds to a custom locale that is the user default, this function returns <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>. If the locale name corresponds to a custom locale that is not the user default, the function returns <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>.

If the locale provided is a transient locale or a CLDR (Unicode Common Locale Data Repository) locale, then the LCID returned is 0x1000.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:
<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>





## -remarks



<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.


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




<a href="https://msdn.microsoft.com/dc776c41-0376-4222-bebf-86be7e4be122">DownlevelLocaleNameToLCID</a>



<a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

