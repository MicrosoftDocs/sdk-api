---
UID: NF:winnls.GetCalendarInfoEx
title: GetCalendarInfoEx function (winnls.h)
author: windows-sdk-content
description: Retrieves information about a calendar for a locale specified by name.Note  The application should call this function in preference to GetCalendarInfo if designed to run only on Windows Vista and later. Note  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
old-location: intl\getcalendarinfoex.htm
tech.root: Intl
ms.assetid: b3c2fb74-0559-4752-9bdb-36b78084aed5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCalendarInfoEx, GetCalendarInfoEx function [Internationalization for Windows Applications], _win32_GetCalendarInfoEx, intl.getcalendarinfoex, winnls/GetCalendarInfoEx
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetCalendarInfoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCalendarInfoEx function


## -description


Retrieves information about a calendar for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/f32ca0d0-8fa2-41e5-9835-76cf51426c3b">GetCalendarInfo</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div>
<div> </div>



## -parameters




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


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a>.


### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.


### -param CalType [in]

Type of information to retrieve. For more information, see <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>. 
			 

<div class="alert"><b>Note</b>  <b>GetCalendarInfoEx</b> returns only one string if this parameter specifies CAL_IYEAROFFSETRANGE or CAL_SERASTRING. In both cases the current era is returned.</div>
<div> </div>
For CAL_NOUSEROVERRIDE, the function ignores any value set by <a href="https://msdn.microsoft.com/3599f68f-5b7c-4bf9-9c42-452047c0731f">SetCalendarInfo</a> and uses the database settings for the current system default locale. This type is relevant only in the combination CAL_NOUSEROVERRIDE | CAL_ITWODIGITYEARMAX. CAL_ITWODIGITYEARMAX is the only value that can be set by <b>SetCalendarInfo</b>.


### -param lpCalData [out, optional]

Pointer to a buffer in which this function retrieves the requested data as a string. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, this parameter must retrieve <b>NULL</b>.


### -param cchData [in]

Size, in characters, of the <i>lpCalData</i> buffer. The application can set this parameter to 0 to return the required size for the calendar data buffer. In this case, the <i>lpCalData</i> parameter is not used. If CAL_RETURN_NUMBER is specified for <i>CalType</i>, the value of <i>cchData</i> must be 0.


### -param lpValue [out, optional]

Pointer to a variable that receives the requested data as a number. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, then <i>lpValue</i> must not be <b>NULL</b>. If CAL_RETURN_NUMBER is not specified in <i>CalType</i>, then <i>lpValue</i> must be <b>NULL</b>.


## -returns



Returns the number of characters retrieved in the <i>lpCalData</i> buffer if successful. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is not specified, the return value is the size of the buffer required to hold the locale information. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is specified, the return value is the size of the value written to the <i>lpValue</i> parameter. This size is always 2.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="https://aka.ms/AA3dzcz">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://docs.microsoft.com/en-us/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>



<a href="https://msdn.microsoft.com/f32ca0d0-8fa2-41e5-9835-76cf51426c3b">GetCalendarInfo</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/3599f68f-5b7c-4bf9-9c42-452047c0731f">SetCalendarInfo</a>
 

 

