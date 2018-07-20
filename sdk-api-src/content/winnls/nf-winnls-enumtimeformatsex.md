---
UID: NF:winnls.EnumTimeFormatsEx
title: EnumTimeFormatsEx function
author: windows-sdk-content
description: Enumerates the time formats that are available for a locale specified by name.Note  The application should call this function in preference to EnumTimeFormats if designed to run only on Windows Vista and later. Note  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
old-location: intl\enumtimeformatsex.htm
old-project: Intl
ms.assetid: db2e297e-98db-4e34-b44c-c0ddcddf2a6e
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: EnumTimeFormatsEx, EnumTimeFormatsEx function [Internationalization for Windows Applications], _win32_EnumTimeFormatsEx, intl.enumtimeformatsex, winnls/EnumTimeFormatsEx
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
api_name:
 - EnumTimeFormatsEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumTimeFormatsEx function


## -description


Enumerates the time formats that are available for a locale specified by name.
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/ad0fe26f-b915-4903-9335-4b268a889c80">EnumTimeFormats</a> if designed to run only on Windows Vista and later.</div><div> </div><div class="alert"><b>Note</b>  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div><div> </div>

## -parameters




### -param lpTimeFmtEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/22725949-2dd3-4382-be22-7ff297925e6b">EnumTimeFormatsProcEx</a>.


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

### -param dwFlags [in]

The time format. Set to 0 to use the current user's long time format, or TIME_NOSECONDS (starting with Windows 7) to use the short time format.


### -param lParam [in]

An application-provided parameter to be passed to the callback function. This is especially useful for multi-threaded applications.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates the time formats by passing time format string pointers, one at a time, to the specified application-defined callback function, along with an application-defined constant that is useful for multi-threaded applications. The first value in the enumeration is always the user default (override) value. The function continues enumeration until the last time format is found or the callback function returns <b>FALSE</b>. 

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad0fe26f-b915-4903-9335-4b268a889c80">EnumTimeFormats</a>



<a href="https://msdn.microsoft.com/22725949-2dd3-4382-be22-7ff297925e6b">EnumTimeFormatsProcEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

