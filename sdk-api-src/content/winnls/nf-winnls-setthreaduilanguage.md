---
UID: NF:winnls.SetThreadUILanguage
title: SetThreadUILanguage function (winnls.h)
description: Sets the user interface language for the current thread.
helpviewer_keywords: ["SetThreadUILanguage","SetThreadUILanguage function [Internationalization for Windows Applications]","_win32_SetThreadUILanguage","intl.setthreaduilanguage","winnls/SetThreadUILanguage"]
old-location: intl\setthreaduilanguage.htm
tech.root: Intl
ms.assetid: 30a0cecf-0ed1-4c03-bd5e-da07b1828c75
ms.date: 12/05/2018
ms.keywords: SetThreadUILanguage, SetThreadUILanguage function [Internationalization for Windows Applications], _win32_SetThreadUILanguage, intl.setthreaduilanguage, winnls/SetThreadUILanguage
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SetThreadUILanguage
 - winnls/SetThreadUILanguage
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - SetThreadUILanguage
---

# SetThreadUILanguage function


## -description

Sets the user interface language for the current thread.

<b>Windows Vista and later:</b> This function cannot clear the thread preferred UI languages list. Your MUI application should call <a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a> to clear the language list.

<b>Windows XP:</b> This function is limited to allowing the operating system to identify and set a value that is safe to use on the Windows console.

## -parameters

### -param LangId [in]

<a href="/windows/desktop/Intl/language-identifiers">Language identifier</a> for the user interface language for the thread.

<b>Windows Vista and later:</b> The application can specify a language identifier of 0 or a nonzero identifier. For more information, see the Remarks section.

<b>Windows XP:</b> The application can only set this parameter to 0. This setting causes the function to select the language that best supports the console display. For more information, see the Remarks section.

## -returns

Returns the input language identifier if successful. If the input identifier is nonzero, the function returns that value. If the language identifier is 0, the function always succeeds and returns the identifier of the language that best supports the Windows console. See the Remarks section.

If the input language identifier is nonzero and the function fails, the return value differs from the input language identifier. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When a thread is created, the thread user interface language setting is empty and the user interface for the thread is displayed in the user-selected language. This function enables the application to change the user interface language for the current running thread.

<b>Windows Vista and later:</b> Calling this function and specifying 0 for the language identifier is identical to calling <a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a> with the MUI_CONSOLE_FILTER flag set. If the application specifies a valid nonzero language identifier, the function sets a particular user interface language for the thread. After specifying 0 for the language identifier, the application cannot use any of the following constants to correspond to a language identifier:


<ul>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
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
<b>Windows XP:</b> When the application calls this function with a language identifier of 0, the function first verifies that the current user interface does not require Uniscribe, and that it is supported by the console <a href="/windows/desktop/Intl/code-pages">code page</a>. If the user interface passes these tests, the function uses the supplied value. If not, the function changes the thread user interface language to a language that the Windows console can display. Windows XP does not support a concept of thread user interface language separate from thread locale. Therefore, this function changes the thread locale on Windows XP. It is easy for your application to set a thread to use the most appropriate language for console display, based on user and system preferred UI languages, the language for non-Unicode applications, and the capabilities of the console.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 SetThreadUILanguage(
            System.UInt16 LangId
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getthreaduilanguage">GetThreadUILanguage</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>