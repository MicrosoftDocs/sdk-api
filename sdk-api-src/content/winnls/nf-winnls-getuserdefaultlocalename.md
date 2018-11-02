---
UID: NF:winnls.GetUserDefaultLocaleName
title: GetUserDefaultLocaleName function
author: windows-sdk-content
description: Retrieves the user default locale name.Note  The application should call this function in preference to GetUserDefaultLCID if designed to run only on Windows Vista and later.
old-location: intl\getuserdefaultlocalename.htm
tech.root: Intl
ms.assetid: 81b896de-1f06-4315-aa64-90806c0fed75
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetUserDefaultLocaleName, GetUserDefaultLocaleName function [Internationalization for Windows Applications], _win32_GetUserDefaultLocaleName, intl.getuserdefaultlocalename, winnls/GetUserDefaultLocaleName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUserDefaultLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetUserDefaultLocaleName function


## -description


Retrieves the user default <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a> if designed to run only on Windows Vista and later.</div>
<div> </div>



## -parameters




### -param lpLocaleName [out]

Pointer to a buffer in which this function retrieves the locale name.


### -param cchLocaleName [in]

Size, in characters, of the buffer indicated by <i>lpLocaleName</i>. The maximum possible length of a locale name, including a terminating null character, is <a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply in this parameter.


## -returns



Returns the size of the buffer containing the locale name, including the terminating null character, if successful.<div class="alert"><b>Note</b>  On single-user systems, the return value is the same as that returned by <a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a>.</div>
<div> </div>


The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
</ul>



## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>



<a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

