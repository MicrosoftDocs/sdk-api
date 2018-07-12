---
UID: NF:winnls.GetCalendarInfoA
title: GetCalendarInfoA function
author: windows-sdk-content
description: Retrieves information about a calendar for a locale specified by identifier.
old-location: intl\getcalendarinfo.htm
old-project: Intl
ms.assetid: f32ca0d0-8fa2-41e5-9835-76cf51426c3b
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetCalendarInfo, GetCalendarInfo function [Internationalization for Windows Applications], GetCalendarInfoA, GetCalendarInfoW, _win32_GetCalendarInfo, intl.getcalendarinfo, winnls/GetCalendarInfo, winnls/GetCalendarInfoA, winnls/GetCalendarInfoW
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
req.unicode-ansi: GetCalendarInfoW (Unicode) and GetCalendarInfoA (ANSI)
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetCalendarInfo
 - GetCalendarInfoA
 - GetCalendarInfoW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCalendarInfoA function


## -description


Retrieves information about a calendar for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/b3c2fb74-0559-4752-9bdb-36b78084aed5">GetCalendarInfoEx</a> function to <b>GetCalendarInfo</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/b3c2fb74-0559-4752-9bdb-36b78084aed5">GetCalendarInfoEx</a>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve calendar information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param Calendar [in]


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a>.


### -param CalType [in]

Type of information to retrieve. For more information, see <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>. 

<div class="alert"><b>Note</b>  <b>GetCalendarInfo</b> returns only one string if this parameter specifies CAL_IYEAROFFSETRANGE or CAL_SERASTRING. In both cases the current era is returned.</div>
<div> </div>
CAL_USE_CP_ACP is relevant only for the ANSI version of this function.

For CAL_NOUSEROVERRIDE, the function ignores any value set by <a href="https://msdn.microsoft.com/3599f68f-5b7c-4bf9-9c42-452047c0731f">SetCalendarInfo</a> and uses the database settings for the current system default locale. This type is relevant only in the combination CAL_NOUSEROVERRIDE | CAL_ITWODIGITYEARMAX. CAL_ITWODIGITYEARMAX is the only value that can be set by <b>SetCalendarInfo</b>.


### -param lpCalData [out, optional]

Pointer to a buffer in which this function retrieves the requested data as a string. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, this parameter must retrieve <b>NULL</b>.


### -param cchData [in]

Size, in characters, of the <i>lpCalData</i> buffer. The application can set this parameter to 0 to return the required size for the calendar data buffer. In this case, the <i>lpCalData</i> parameter is not used. If CAL_RETURN_NUMBER is specified for <i>CalType</i>, the value of <i>cchData</i> must be 0.


### -param lpValue [out, optional]

Pointer to a variable that receives the requested data as a number. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, then <i>lpValue</i> must not be <b>NULL</b>. If CAL_RETURN_NUMBER is not specified in <i>CalType</i>, then <i>lpValue</i> must be <b>NULL</b>.


## -returns



Returns the number of characters retrieved in the <i>lpCalData</i> buffer, with <i>cchData</i> set to a nonzero value, if successful. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is not specified, the return value is the size of the buffer required to hold the calendar information. If the function succeeds, <i>cchData</i> is set 0, and CAL_RETURN_NUMBER is specified, the return value is the size of the value retrieved in <i>lpValue</i>, that is, 2 for the Unicode version of the function or 4 for the ANSI version.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 




## -see-also




<a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>



<a href="https://msdn.microsoft.com/b3c2fb74-0559-4752-9bdb-36b78084aed5">GetCalendarInfoEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/3599f68f-5b7c-4bf9-9c42-452047c0731f">SetCalendarInfo</a>
 

 

