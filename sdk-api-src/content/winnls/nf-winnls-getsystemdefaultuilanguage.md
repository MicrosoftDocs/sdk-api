---
UID: NF:winnls.GetSystemDefaultUILanguage
title: GetSystemDefaultUILanguage function (winnls.h)
description: Retrieves the language identifier for the system default UI language of the operating system, also known as the &quot;install language&quot; on Windows Vista and later. For more information, see User Interface Language Management.
helpviewer_keywords: ["GetSystemDefaultUILanguage","GetSystemDefaultUILanguage function [Internationalization for Windows Applications]","_win32_GetSystemDefaultUILanguage","intl.getsystemdefaultuilanguage","winnls/GetSystemDefaultUILanguage"]
old-location: intl\getsystemdefaultuilanguage.htm
tech.root: Intl
ms.assetid: 34fc125d-0f0b-43d0-aa2b-91501bd6cd26
ms.date: 09/24/2020
ms.keywords: GetSystemDefaultUILanguage, GetSystemDefaultUILanguage function [Internationalization for Windows Applications], _win32_GetSystemDefaultUILanguage, intl.getsystemdefaultuilanguage, winnls/GetSystemDefaultUILanguage
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
 - GetSystemDefaultUILanguage
 - winnls/GetSystemDefaultUILanguage
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
api_name:
 - GetSystemDefaultUILanguage
---

# GetSystemDefaultUILanguage function

## -description

Retrieves the [language identifier](/windows/desktop/Intl/language-identifiers) for the system default UI language of the operating system (also known as the "install language" on Windows Vista and later). For more information, see [User Interface Language Management](/windows/desktop/Intl/user-interface-language-management).

> [!Important]
> Use of this function is not recommended. Instead, we recommend using the [User language settings](/windows/win32/intl/setting-application-language-preferences) for the following reasons.
>
> - "Install language" is only set during the Out of Box Experience (OOBE) and then never changes. If the system language is changed, this function returns an incorrect value.
> - WCOS SKUs always return an incorrect value.
> - This function uses deprecated LANGIDs.



## -returns

Returns the language identifier for the system default UI language of the operating system. For more information, see the Remarks section.

## -remarks

This function never returns a language identifier for a Language Interface Pack (LIP). It also never returns a language identifier corresponding to the locale identifier [LOCALE_CUSTOM_UNSPECIFIED](/windows/desktop/Intl/locale-custom-constants) or [LOCALE_CUSTOM_UI_DEFAULT](/windows/desktop/Intl/locale-custom-constants).

Note that this function does not necessarily return the identifier for the first language in the system preferred UI languages list. Therefore the return might not match the first element retrieved by [GetSystemPreferredUILanguages](/windows/desktop/api/winnls/nf-winnls-getsystempreferreduilanguages).

### C# Signature

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetSystemDefaultUILanguage();

```

## -see-also

[EnumUILanguages](/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa), [GetSystemPreferredUILanguages](/windows/desktop/api/winnls/nf-winnls-getsystempreferreduilanguages), [GetUserDefaultUILanguage](/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage), [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface), [Multilingual User Interface Functions](/windows/desktop/Intl/multilingual-user-interface-functions)
