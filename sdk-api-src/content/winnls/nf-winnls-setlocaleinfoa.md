---
UID: NF:winnls.SetLocaleInfoA
title: SetLocaleInfoA function
author: windows-driver-content
description: Sets an item of information in the user override portion of the current locale. This function does not set the system defaults.
old-location: intl\setlocaleinfo.htm
old-project: Intl
ms.assetid: 96e031cb-0d9f-4556-b9b3-3451d8f80da5
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: SetLocaleInfo, SetLocaleInfo function [Internationalization for Windows Applications], SetLocaleInfoA, SetLocaleInfoW, _win32_SetLocaleInfo, intl.setlocaleinfo, winnls/SetLocaleInfo, winnls/SetLocaleInfoA, winnls/SetLocaleInfoW
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
req.unicode-ansi: SetLocaleInfoW (Unicode) and SetLocaleInfoA (ANSI)
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
-	Kernel32.dll
-	API-MS-Win-Core-Localization-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-l1-2-0.dll
-	API-MS-Win-Core-Localization-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-L1-2-2.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	SetLocaleInfo
-	SetLocaleInfoA
-	SetLocaleInfoW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetLocaleInfoA function


## -description


Sets an item of information in the user override portion of the current locale. This function does not set the system defaults.
<div class="alert"><b>Caution</b>  Because this function modifies values for all applications, it should only be called by the regional and language options functionality of Control Panel, or a similar utility. If making an international change to system parameters, the calling application must broadcast the <a href="https://msdn.microsoft.com/77174e06-a25b-440a-9e9c-4fd5979c433c">WM_SETTINGCHANGE</a> message to avoid causing instabilities in other applications.</div><div> </div>

## -parameters




### -param Locale [in]

For the ANSI version of the function, the <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> of the locale with the code page used when interpreting the <i>lpLCData</i> information. For the Unicode version, this parameter is ignored.

You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

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
The following custom locale identifiers are also supported.

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

### -param LCType [in]

Type of locale information to set. For valid constants see "Constants Used in the LCType Parameter of GetLocaleInfo, GetLocaleInfoEx, and SetLocaleInfo" section of <a href="https://msdn.microsoft.com/45798dd1-34bb-4e99-8f84-94f28e76711f">Locale Information Constants</a>. The application can specify only one value per call, but it can use the binary OR operator to combine <a href="https://msdn.microsoft.com/686ca9f2-515d-449f-8871-77c78ab5c31a">LOCALE_USE_CP_ACP</a> with any other constant. 



### -param lpLCData [in]

Pointer to a null-terminated string containing the locale information to set. The information must be in the format specific to the specified constant. The application uses a Unicode string for the Unicode version of the function, and an ANSI string for the ANSI version.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_ACCESS_DISABLED_BY_POLICY. The group policy of the computer or the user has forbidden this operation.</li>
<li>ERROR_INVALID_ACCESS. The access code was invalid.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function writes to the registry, where it sets values that are associated with a particular user instead of a particular application. These registry values affect the behavior of other applications run by the user. As a rule, an application should call this function only when the user has explicitly requested the changes. The registry settings should not be changed for the convenience of a single application.

For the <i>LCType</i> parameter, the application should set <a href="https://msdn.microsoft.com/686ca9f2-515d-449f-8871-77c78ab5c31a">LOCALE_USE_CP_ACP</a> to use the operating system ANSI code page instead of the locale code page for string translation.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 


        As of Windows Vista, the <a href="https://msdn.microsoft.com/18b62bee-b167-4499-aae4-21e215cb6377">LOCALE_SDATE</a> and <a href="https://msdn.microsoft.com/d16e7e0c-93f1-4f08-a319-02b717b7d33b">LOCALE_STIME</a> constants are obsolete. Do not use these constants. Use <a href="https://msdn.microsoft.com/55333a53-1205-42eb-aa1a-c248c52a8a3f">LOCALE_SSHORTDATE</a> and <a href="https://msdn.microsoft.com/d16e7e0c-93f1-4f08-a319-02b717b7d33b">LOCALE_STIMEFORMAT</a> instead. A custom locale might not have a single, uniform separator character within the date or time format: for example, a format such as "12/31, 2006" or "03:56'23" might be valid.




## -see-also




<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

