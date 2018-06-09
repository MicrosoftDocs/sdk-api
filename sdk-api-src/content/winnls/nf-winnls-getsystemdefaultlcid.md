---
UID: NF:winnls.GetSystemDefaultLCID
title: GetSystemDefaultLCID function
author: windows-sdk-content
description: Returns the locale identifier for the system locale.Note  Any application that runs only on Windows Vista and later should use GetSystemDefaultLocaleName in preference to this function.
old-location: intl\getsystemdefaultlcid.htm
old-project: Intl
ms.assetid: 67d73d88-6a6c-439b-a321-1b1bd05fe268
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSystemDefaultLCID, GetSystemDefaultLCID function [Internationalization for Windows Applications], _win32_GetSystemDefaultLCID, intl.getsystemdefaultlcid, winnls/GetSystemDefaultLCID
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
 - GetSystemDefaultLCID
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetSystemDefaultLCID function


## -description


Returns the <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> for the system locale.<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a> in preference to this function.</div>
<div> </div>



## -parameters






## -returns



Returns the locale identifier for the system default locale, identified by <a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>.




## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/e227bb9f-f072-4e44-bd55-24c98b990a36">ConvertDefaultLocale</a>



<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

