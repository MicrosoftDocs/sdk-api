---
UID: NF:winnls.GetSystemDefaultUILanguage
title: GetSystemDefaultUILanguage function (winnls.h)
author: windows-sdk-content
description: Retrieves the language identifier for the system default UI language of the operating system, also known as the &#0034;install language&#0034; on Windows Vista and later. For more information, see User Interface Language Management.
old-location: intl\getsystemdefaultuilanguage.htm
tech.root: Intl
ms.assetid: 34fc125d-0f0b-43d0-aa2b-91501bd6cd26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemDefaultUILanguage, GetSystemDefaultUILanguage function [Internationalization for Windows Applications], _win32_GetSystemDefaultUILanguage, intl.getsystemdefaultuilanguage, winnls/GetSystemDefaultUILanguage
ms.topic: function
f1_keywords: ["winnls/GetSystemDefaultUILanguage"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemDefaultUILanguage function


## -description


Retrieves the <a href="https://docs.microsoft.com/windows/desktop/Intl/language-identifiers">language identifier</a> for the system default UI language of the operating system, also known as the "install language" on Windows Vista and later. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>.


## -parameters






## -returns



Returns the language identifier for the system default UI language of the operating system. For more information, see the Remarks section.




## -remarks



This function never returns a language identifier for a Language Interface Pack (LIP). It also never returns a language identifier corresponding to the locale identifier <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a> or <a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>.

Note that this function does not necessarily return the identifier for the first language in the system preferred UI languages list. Therefore the return might not match the first element retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getsystempreferreduilanguages">GetSystemPreferredUILanguages</a>.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.UInt16 GetSystemDefaultUILanguage();

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getsystempreferreduilanguages">GetSystemPreferredUILanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage">GetUserDefaultUILanguage</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>
 

 

