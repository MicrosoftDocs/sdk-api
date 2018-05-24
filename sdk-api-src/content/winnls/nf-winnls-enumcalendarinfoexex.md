---
UID: NF:winnls.EnumCalendarInfoExEx
title: EnumCalendarInfoExEx function
author: windows-driver-content
description: Enumerates calendar information for a locale specified by name.Note  The application should call this function in preference to EnumCalendarInfo or EnumCalendarInfoEx if designed to run only on Windows Vista and later. Note  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
old-location: intl\enumcalendarinfoexex.htm
old-project: Intl
ms.assetid: 2aa4d5b8-9afc-4657-92f0-d5d61791b807
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: EnumCalendarInfoExEx, EnumCalendarInfoExEx function [Internationalization for Windows Applications], _win32_EnumCalendarInfoExEx, intl.enumcalendarinfoexex, winnls/EnumCalendarInfoExEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	Kernel32.dll
-	API-MS-Win-Core-Localization-l2-1-0.dll
-	KernelBase.dll
api_name:
-	EnumCalendarInfoExEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumCalendarInfoExEx function


## -description


Enumerates calendar information for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a> or <a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div>
<div> </div>



## -parameters




### -param pCalInfoEnumProcExEx [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/26368cb9-6d1d-4ab1-a8f2-831c1ef4398a">EnumCalendarInfoProcExEx</a>.


### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

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

### -param Calendar [in]


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a> that specifies the calendar for which information is requested. Note that this identifier can be ENUM_ALL_CALENDARS, to enumerate all calendars that are associated with the locale.


### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.


### -param CalType [in]

Type of calendar information. For more information, see <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>. Only one calendar type can be specified per call to this function, except where noted.


### -param lParam [in]

Application-provided parameter to pass to the callback function. This value is especially useful for multi-threaded applications.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates calendar information for all applicable calendars for the specified locale, or for a single requested calendar, depending on the value of the <i>Calendar</i> parameter. The function enumerates the calendar information by calling the specified application-defined callback function. It passes the callback function a pointer to a buffer containing the requested calendar information, a calendar identifier, and an application-defined parameter that is useful for multi-threaded applications. This process continues until <b>EnumCalendarInfoExEx</b> finds the last applicable calendar or the callback function returns <b>FALSE</b>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>



<a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a>



<a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a>



<a href="https://msdn.microsoft.com/26368cb9-6d1d-4ab1-a8f2-831c1ef4398a">EnumCalendarInfoProcExEx</a>



<a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

