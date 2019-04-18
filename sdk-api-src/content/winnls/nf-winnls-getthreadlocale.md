---
UID: NF:winnls.GetThreadLocale
title: GetThreadLocale function (winnls.h)
author: windows-sdk-content
description: Returns the locale identifier of the current locale for the calling thread.Note  This function can retrieve data that changes between releases, for example, due to a custom locale.
old-location: intl\getthreadlocale.htm
tech.root: Intl
ms.assetid: 4d77f78b-f059-40f3-b4ed-c3ffd09d9e9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThreadLocale, GetThreadLocale function [Internationalization for Windows Applications], _win32_GetThreadLocale, intl.getthreadlocale, winnls/GetThreadLocale
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetThreadLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadLocale function


## -description


Returns the <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> of the current locale for the calling thread.<div class="alert"><b>Note</b>  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div>
<div> </div>



## -parameters






## -returns



Returns the <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> of the locale associated with the current thread.

<b>Windows Vista</b>: This function can return the identifier of a <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locale</a>. If the current thread locale is a custom locale, the function returns <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>. If the current thread locale is a supplemental custom locale, the function can return <a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>. All supplemental locales share this locale identifier.




## -remarks



When an application process launches, it uses the Standards and Formats variable for the locale. For more information, see <a href="https://msdn.microsoft.com/daf929b2-8ff9-4a17-b294-f2c0eaef5848">NLS Terminology</a>.

When a new thread is created in a process, it inherits the locale of the creating thread. This locale can be either the default Standards and Formats locale or a different locale set for the creating thread in a call to <a href="https://msdn.microsoft.com/d86193c7-9b3a-422b-b76c-ff1992f68958">SetThreadLocale</a>. <b>GetThreadLocale</b> and <b>SetThreadLocale</b> can be used to modify the locale of the new thread.




## -see-also




<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/d86193c7-9b3a-422b-b76c-ff1992f68958">SetThreadLocale</a>
 

 

