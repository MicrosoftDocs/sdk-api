---
UID: NF:winnls.LCIDToLocaleName
title: LCIDToLocaleName function
author: windows-sdk-content
description: Converts a locale identifier to a locale name.
old-location: intl\lcidtolocalename.htm
old-project: Intl
ms.assetid: 63233e3e-5b7c-43cb-9c62-88b0791c2647
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LCIDToLocaleName, LCIDToLocaleName function [Internationalization for Windows Applications], _win32_LCIDToLocaleName, intl.lcidtolocalename, winnls/LCIDToLocaleName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.redist: 
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
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - LCIDToLocaleName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LCIDToLocaleName function


## -description


Converts a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>. <div class="alert"><b>Note</b>  For custom locales, including those created by Microsoft, your applications should prefer locale names over locale identifiers.</div>
<div> </div>



## -parameters




### -param Locale [in]

Locale identifier to translate. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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
<b>Windows Vista:</b> The following custom locale identifiers are also supported.

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

### -param lpName [out, optional]

Pointer to a buffer in which this function retrieves the locale name, or one of the following predefined values. 

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

### -param cchName [in]

Size, in characters, of the locale name buffer. The maximum possible length of a locale name, including a terminating null character, is <a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply for this parameter.

Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the locale name buffer.


### -param dwFlags [in]

<b>Before Windows 7:</b> Reserved; should always be 0.

<b>Starting with Windows 7:</b> Can be set to <a href="https://msdn.microsoft.com/b4f9d07c-3c39-46aa-933d-5c8c6ae98345">LOCALE_ALLOW_NEUTRAL_NAMES</a> to allow the return of a neutral name.


## -returns



Returns the count of characters, including the terminating null character, in the locale name if successful. If the function succeeds and the value of <i>cchName</i> is 0, the return value is the required size, in characters (including nulls), for the locale name buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/00404566-b9ef-43ea-8056-ca9ab0117814">LocaleNameToLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

