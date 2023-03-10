---
UID: NF:winnls.GetUserDefaultUILanguage
title: GetUserDefaultUILanguage function (winnls.h)
description: Returns the language identifier for the user UI language for the current user.
helpviewer_keywords: ["GetUserDefaultUILanguage","GetUserDefaultUILanguage function [Internationalization for Windows Applications]","_win32_GetUserDefaultUILanguage","intl.getuserdefaultuilanguage","winnls/GetUserDefaultUILanguage"]
old-location: intl\getuserdefaultuilanguage.htm
tech.root: Intl
ms.assetid: 0de3a2d8-e595-4068-805c-b9bcba7ada91
ms.date: 12/05/2018
ms.keywords: GetUserDefaultUILanguage, GetUserDefaultUILanguage function [Internationalization for Windows Applications], _win32_GetUserDefaultUILanguage, intl.getuserdefaultuilanguage, winnls/GetUserDefaultUILanguage
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetUserDefaultUILanguage
 - winnls/GetUserDefaultUILanguage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetUserDefaultUILanguage
---

# GetUserDefaultUILanguage function


## -description

Returns the language identifier for the user UI language for the current user. If the current user has not set a language, <b>GetUserDefaultUILanguage</b> returns the preferred language set for the system. If there is no preferred language set for the system, then the system default UI language (also known as "install language") is returned. For more information about the user UI language, see <a href="/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.



## -returns

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the user UI language for the current user.

## -remarks

This function returns only a language identifier. An application can retrieve the language name using the <a href="/windows/desktop/api/winnls/nf-winnls-getuserpreferreduilanguages">GetUserPreferredUILanguages</a> function.

If the user UI language is part of a Language Interface Pack (LIP) and corresponds to a <a href="/windows/desktop/Intl/custom-locales">supplemental locale</a>, this function returns <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>.

<b>Windows Me, Windows 2000, Windows XP, Windows Server 2003:</b> The <b>GetUserDefaultUILanguage</b> function retrieves the language identifier for the current user language. If MUI is not installed on the operating system, the function retrieves the default computer user interface language.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetUserDefaultUILanguage();

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultuilanguage">GetSystemDefaultUILanguage</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>
