---
UID: NF:winnls.GetThreadUILanguage
title: GetThreadUILanguage function (winnls.h)
description: Returns the language identifier of the first user interface language for the current thread.
helpviewer_keywords: ["GetThreadUILanguage","GetThreadUILanguage function [Internationalization for Windows Applications]","_win32_GetThreadUILanguage","intl.getthreaduilanguage","winnls/GetThreadUILanguage"]
old-location: intl\getthreaduilanguage.htm
tech.root: Intl
ms.assetid: c10cbf84-8aaf-46c7-8b2f-e719e30f2556
ms.date: 12/05/2018
ms.keywords: GetThreadUILanguage, GetThreadUILanguage function [Internationalization for Windows Applications], _win32_GetThreadUILanguage, intl.getthreaduilanguage, winnls/GetThreadUILanguage
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
 - GetThreadUILanguage
 - winnls/GetThreadUILanguage
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
 - GetThreadUILanguage
---

# GetThreadUILanguage function


## -description

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> of the first user interface language for the current thread.



## -returns

Returns the identifier for a language explicitly associated with the thread by <a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a> or <a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>. Alternatively, if no language has been explicitly associated with the current thread, the identifier can indicate a user or system user interface language.

## -remarks

Calling this function is identical to calling <a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a> with <i>dwFlags</i> set to MUI_MERGE_SYSTEM_FALLBACK | MUI_MERGE_USER_FALLBACK | MUI_LANGUAGE_ID and using the first language in the retrieved list.

The return value for this function does not provide useful information about a Language Interface Pack (LIP) language if that language corresponds to a <a href="/windows/desktop/Intl/custom-locales">supplemental locale</a>. For such a language, the function returns the hexadecimal value "1400", which corresponds to <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a> if that language is specified in the user preferred UI languages list. If the language is not specified in the user preferred UI languages list, the function returns the value "1000", corresponding to <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetThreadUILanguage();

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getthreadpreferreduilanguages">GetThreadPreferredUILanguages</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>
