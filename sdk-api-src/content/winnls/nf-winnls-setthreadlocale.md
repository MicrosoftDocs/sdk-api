---
UID: NF:winnls.SetThreadLocale
title: SetThreadLocale function (winnls.h)
description: Sets the current locale of the calling thread.
helpviewer_keywords: ["SetThreadLocale","SetThreadLocale function [Internationalization for Windows Applications]","_win32_SetThreadLocale","intl.setthreadlocale","winnls/SetThreadLocale"]
old-location: intl\setthreadlocale.htm
tech.root: Intl
ms.assetid: d86193c7-9b3a-422b-b76c-ff1992f68958
ms.date: 12/05/2018
ms.keywords: SetThreadLocale, SetThreadLocale function [Internationalization for Windows Applications], _win32_SetThreadLocale, intl.setthreadlocale, winnls/SetThreadLocale
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
 - SetThreadLocale
 - winnls/SetThreadLocale
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
 - SetThreadLocale
---

# SetThreadLocale function


## -description

Sets the current locale of the calling thread.

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

## -returns

The function should return an LCID on success. This is the LCID of the previous thread locale.

## -remarks

When a thread is created, it uses the user locale. This value is returned by <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>. The user locale can be modified for future processes and thread creation using the regional and language options portion of the Control Panel. The thread locale can also be changed using <b>SetThreadLocale</b>.

<b>SetThreadLocale</b> affects the selection of resources with a <a href="/windows/desktop/menurc/language-statement">LANGUAGE</a> statement. The statement affects such functions as <a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a>, <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadmenua">LoadMenu</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>, and <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>. It sets the code page implied by CP_THREAD_ACP, but does not affect <a href="/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>. For more information, see <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>.

<b>Windows Vista and later: </b> Do not use <b>SetThreadLocale</b> to select a user interface language. The resource loader selects the resource that is defined in the .rc file with a <a href="/windows/desktop/menurc/language-statement">LANGUAGE</a> statement, or the application can use <a href="/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>. Additionally, the application can use <a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>.
      

<b>Windows 2000, Windows XP:</b> Do not use <b>SetThreadLocale</b> to select a user interface language. To select the resource that is defined in the .rc file with a <a href="/windows/desktop/menurc/language-statement">LANGUAGE</a> statement, the application must use the <a href="/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> function.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getthreadlocale">GetThreadLocale</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>