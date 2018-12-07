---
UID: NF:winnls.GetSystemDefaultLocaleName
title: GetSystemDefaultLocaleName function
author: windows-sdk-content
description: Retrieves the system default locale name.Note  It is recommended that applications call GetUserDefaultLocaleName in preference over this function.
old-location: intl\getsystemdefaultlocalename.htm
tech.root: Intl
ms.assetid: 1e925e41-64db-44aa-ab73-05d0f2036c8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSystemDefaultLocaleName, GetSystemDefaultLocaleName function [Internationalization for Windows Applications], _win32_GetSystemDefaultLocaleName, intl.getsystemdefaultlocalename, winnls/GetSystemDefaultLocaleName
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
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetSystemDefaultLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemDefaultLocaleName function


## -description


Retrieves the system default <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>.<div class="alert"><b>Note</b>  It is recommended that applications call <a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a> in preference over this function. This is due to the user locale generally being more useful and accurate for the user than the system locale.</div>
<div> </div>
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a> if designed to run only on Windows Vista and later.</div>
<div> </div>



## -parameters




### -param lpLocaleName [out]

Pointer to a buffer in which this function retrieves the locale name.


### -param cchLocaleName [in]

Size, in characters, of the output buffer indicated by <i>lpLocaleName</i>. The maximum possible character length of a locale name (including a terminating null character) is the value of <a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size.


## -returns



Returns a value greater than 0 that indicates the length of the locale name, including the terminating null character, if successful.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>



## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.


#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8e40d097-08a2-43e8-88e8-a4ecaddf449a">DownlevelLCIDToLocaleName</a>



<a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>



<a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/01bc261d-dfee-430e-86c9-cfafe82856c8">Mapping Locale Data</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

