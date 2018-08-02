---
UID: NF:winnls.GetUserDefaultLCID
title: GetUserDefaultLCID function
author: windows-sdk-content
description: Returns the locale identifier for the user default locale.Caution  If the user default locale is a custom locale, an application cannot accurately tag data with the value or exchange it.
old-location: intl\getuserdefaultlcid.htm
old-project: Intl
ms.assetid: bbf8399e-9034-4480-8d6e-030714f94e48
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetUserDefaultLCID, GetUserDefaultLCID function [Internationalization for Windows Applications], _win32_GetUserDefaultLCID, intl.getuserdefaultlcid, winnls/GetUserDefaultLCID
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUserDefaultLCID
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUserDefaultLCID function


## -description


Returns the <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> for the user default locale.
<div class="alert"><b>Caution</b>  If the user default locale is a custom locale, an application cannot accurately tag data with the value or exchange it. In this case, the application should use  <a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a> in preference to <b>GetUserDefaultLCID</b>.</div><div> </div><div class="alert"><b>Note</b>  Applications that are intended to run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a>.</div><div> </div>

## -parameters






## -returns



Returns the locale identifier for the user default locale, represented as <a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>. If the user default locale is a custom locale, this function always returns <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>, regardless of the custom locale that is selected. For example, whether the user locale is Hawaiian (US), haw-US, or Fijiian (Fiji), fj-FJ, the function returns the same value.




## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/e227bb9f-f072-4e44-bd55-24c98b990a36">ConvertDefaultLocale</a>



<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

