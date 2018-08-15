---
UID: NF:datetimeapi.GetDateFormatW
title: GetDateFormatW function
author: windows-sdk-content
description: Formats a date as a date string for a locale specified by the locale identifier.
old-location: intl\getdateformat.htm
old-project: Intl
ms.assetid: 546cede1-1702-403a-bba3-b5cd3b35a1bf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDateFormat, GetDateFormat function [Internationalization for Windows Applications], GetDateFormatA, GetDateFormatW, _win32_GetDateFormat, datetimeapi/GetDateFormat, datetimeapi/GetDateFormatA, datetimeapi/GetDateFormatW, intl.getdateformat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: datetimeapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDateFormatW (Unicode) and GetDateFormatA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3DX11_FFT_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-datetime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-datetime-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-DateTime-L1-1-2.dll
api_name:
 - GetDateFormat
 - GetDateFormatA
 - GetDateFormatW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetDateFormatW function


## -description


Formats a date as a date string for a locale specified by the locale identifier. The function formats either a specified date or the local system date.
      <div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/791fb386-3cc5-410e-bfce-52598fdb10c9">GetDateFormatEx</a> function to <b>GetDateFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/791fb386-3cc5-410e-bfce-52598fdb10c9">GetDateFormatEx</a>.</div>
<div> </div>



## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale this function formats the date string for. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param dwFlags [in]

Flags specifying date format options. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/791fb386-3cc5-410e-bfce-52598fdb10c9">GetDateFormatEx</a>.


### -param lpDate [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date information to format. The application sets this parameter to <b>NULL</b> if the function is to use the current local system date.


### -param lpFormat [in, optional]

Pointer to a format picture string that is used to form the date. Possible values for the format picture string are defined in <a href="https://msdn.microsoft.com/c18868a9-6912-46fd-93f5-d8021937b049">Day, Month, Year, and Era Format Pictures</a>.

The function uses the specified locale only for information not specified in the format picture string, for example, the day and month names for the locale. The application can set this parameter to <b>NULL</b> to format the string according to the date format for the specified locale.


### -param lpDateStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted date string.


### -param cchDate [in]

Size, in characters, of the <i>lpDateStr</i> buffer. The application can set this parameter to 0 to return the buffer size required to hold the formatted date string. In this case, the buffer indicated by <i>lpDateStr</i> is not used.


## -returns



Returns the number of characters written to the <i>lpDateStr</i> buffer if successful. If the <i>cchDate</i> parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/791fb386-3cc5-410e-bfce-52598fdb10c9">GetDateFormatEx</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark ("?"). 
      

<b>Starting with Windows 8: </b><b>GetDateFormat</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.




## -see-also




<a href="https://msdn.microsoft.com/c18868a9-6912-46fd-93f5-d8021937b049">Day, Month, Year, and Era Format Pictures</a>



<a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a>



<a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a>



<a href="https://msdn.microsoft.com/f32ca0d0-8fa2-41e5-9835-76cf51426c3b">GetCalendarInfo</a>



<a href="https://msdn.microsoft.com/791fb386-3cc5-410e-bfce-52598fdb10c9">GetDateFormatEx</a>



<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/3db91d29-df97-4660-b3cd-0db5b42cfd01">GetTimeFormat</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

