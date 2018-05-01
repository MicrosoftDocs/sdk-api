---
UID: NF:winnls.ConvertDefaultLocale
title: ConvertDefaultLocale function
author: windows-driver-content
description: Converts a default locale value to an actual locale identifier.
old-location: intl\convertdefaultlocale.htm
old-project: Intl
ms.assetid: e227bb9f-f072-4e44-bd55-24c98b990a36
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ConvertDefaultLocale, ConvertDefaultLocale function [Internationalization for Windows Applications], _win32_ConvertDefaultLocale, intl.convertdefaultlocale, winnls/ConvertDefaultLocale
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-Localization-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-l1-2-0.dll
-	API-MS-Win-Core-Localization-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
-	ConvertDefaultLocale
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ConvertDefaultLocale function


## -description


Converts a default locale value to an actual <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a>.
<div class="alert"><b>Note</b>  
         This function is only provided for converting partial locale identifiers. Your applications should use locale names instead of identifiers. The <a href="https://msdn.microsoft.com/63233e3e-5b7c-43cb-9c62-88b0791c2647">LCIDToLocaleName</a> function can be used to convert a locale identifier to a valid locale name. Your application can also use <a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a> to retrieve the current user locale name; <a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a> to retrieve the current system locale name; and <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a> with <a href="https://msdn.microsoft.com/9823f675-8dc8-42c1-938f-22910434694e">LOCALE_SNAME</a> to retrieve the locale name for any input locale, including the default constants.</div><div> </div>

## -parameters




### -param Locale [in]

Default locale identifier value to convert. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

## -returns



Returns the appropriate locale identifier if successful.

This function returns the value of the <i>Locale</i> parameter if it does not succeed. The function fails when the <i>Locale</i> value is not one of the default values listed above.




## -remarks



A call to <b>ConvertDefaultLocale</b> specifying LOCALE_SYSTEM_DEFAULT is equivalent to a call to <a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>. A call to <b>ConvertDefaultLocale</b> specifying LOCALE_USER_DEFAULT is equivalent to a call to <a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>.




## -see-also




<a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>



<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/63233e3e-5b7c-43cb-9c62-88b0791c2647">LCIDToLocaleName</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

