---
UID: NF:winnls.EnumLanguageGroupLocalesA
title: EnumLanguageGroupLocalesA function
author: windows-sdk-content
description: Enumerates the locales in a specified language group.
old-location: intl\enumlanguagegrouplocales.htm
old-project: Intl
ms.assetid: 5a85c6bd-0362-46ff-80be-a198b1259482
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumLanguageGroupLocales, EnumLanguageGroupLocales function [Internationalization for Windows Applications], EnumLanguageGroupLocalesA, EnumLanguageGroupLocalesW, _win32_EnumLanguageGroupLocales, intl.enumlanguagegrouplocales, winnls/EnumLanguageGroupLocales, winnls/EnumLanguageGroupLocalesA, winnls/EnumLanguageGroupLocalesW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumLanguageGroupLocalesW (Unicode) and EnumLanguageGroupLocalesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumLanguageGroupLocales
 - EnumLanguageGroupLocalesA
 - EnumLanguageGroupLocalesW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumLanguageGroupLocalesA function


## -description


Enumerates the locales in a specified language group. <div class="alert"><b>Note</b>  For custom locales, your application should call <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a> in preference to <b>EnumLanguageGroupLocales</b>.</div>
<div> </div>



## -parameters




### -param lpLangGroupLocaleEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/e422c61f-7a97-4f95-8592-22a1eb5f616b">EnumLanguageGroupLocalesProc</a>.


### -param LanguageGroup [in]

Identifier of the language group for which to enumerate locales. This parameter can have one of the following values:

<ul>
<li>LGRPID_ARABIC
</li>
<li>LGRPID_ARMENIAN</li>
<li>LGRPID_BALTIC
</li>
<li>LGRPID_CENTRAL_EUROPE
</li>
<li>LGRPID_CYRILLIC
</li>
<li>LGRPID_GEORGIAN
</li>
<li>LGRPID_GREEK
</li>
<li>LGRPID_HEBREW
</li>
<li>LGRPID_INDIC
</li>
<li>LGRPID_JAPANESE
</li>
<li>LGRPID_KOREAN
</li>
<li>LGRPID_SIMPLIFIED_CHINESE
</li>
<li>LGRPID_TRADITIONAL_CHINESE</li>
<li>LGRPID_THAI
</li>
<li>LGRPID_TURKIC</li>
<li>LGRPID_TURKISH
</li>
<li>LGRPID_VIETNAMESE
</li>
<li>LGRPID_WESTERN_EUROPE
</li>
</ul>

### -param dwFlags [in]

Reserved; must be 0.


### -param lParam [in]

An application-defined value to pass to the callback function. This value can be used for error checking. It can also be used to ensure thread safety in the callback function.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates locales in the specified language group by passing locale identifiers, one at a time, to the application-defined callback function. This process continues until <b>EnumLanguageGroupLocales</b> finds the last locale identifier or the callback function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/e422c61f-7a97-4f95-8592-22a1eb5f616b">EnumLanguageGroupLocalesProc</a>



<a href="https://msdn.microsoft.com/8cc2335e-b222-44d9-a966-4b6803639071">EnumSystemLanguageGroups</a>



<a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a>



<a href="https://msdn.microsoft.com/68cf09f8-fe97-4035-94b6-886ca26bbf3e">IsValidLanguageGroup</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

