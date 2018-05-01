---
UID: NF:datetimeapi.GetTimeFormatA
title: GetTimeFormatA function
author: windows-driver-content
description: Formats time as a time string for a locale specified by identifier. The function formats either a specified time or the local system time.
old-location: intl\gettimeformat.htm
old-project: Intl
ms.assetid: 3db91d29-df97-4660-b3cd-0db5b42cfd01
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetTimeFormat, GetTimeFormat function [Internationalization for Windows Applications], GetTimeFormatA, GetTimeFormatW, _win32_GetTimeFormat, datetimeapi/GetTimeFormat, datetimeapi/GetTimeFormatA, datetimeapi/GetTimeFormatW, intl.gettimeformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: datetimeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTimeFormatW (Unicode) and GetTimeFormatA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DX11_FFT_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-datetime-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-datetime-l1-1-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-DateTime-L1-1-2.dll
api_name:
-	GetTimeFormat
-	GetTimeFormatA
-	GetTimeFormatW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetTimeFormatA function


## -description


Formats time as a time string for a locale specified by identifier. The function formats either a specified time or the local system time.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/4d63888e-4496-4315-ac87-bf60c54daa37">GetTimeFormatEx</a> function to <b>GetTimeFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/4d63888e-4496-4315-ac87-bf60c54daa37">GetTimeFormatEx</a>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

Flags specifying time format options. For detailed definitions see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/4d63888e-4496-4315-ac87-bf60c54daa37">GetTimeFormatEx</a>.


### -param lpTime [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the time information to format. The application can set this parameter to <b>NULL</b> if the function is to use the current local system time.


### -param lpFormat [in, optional]

Pointer to a format picture to use to format the time string. If the application sets this parameter to <b>NULL</b>, the function formats the string according to the time format of the specified locale. If the application does not set the parameter to <b>NULL</b>, the function uses the locale only for information not specified in the format picture string, for example, the locale-specific time markers. For information about the format picture string, see the Remarks section.


### -param lpTimeStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted time string.


### -param cchTime [in]

Size, in TCHAR values, for the time string buffer indicated by <i>lpTimeStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the time string buffer, and does not use the <i>lpTimeStr</i> parameter.


## -returns



Returns the number of TCHAR values retrieved in the buffer indicated by <i>lpTimeStr</i>. If the <i>cchTime</i> parameter is set to 0, the function returns the size of the buffer required to hold the formatted time string, including a terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/4d63888e-4496-4315-ac87-bf60c54daa37">GetTimeFormatEx</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      

<b>Starting with Windows 8: </b><b>GetTimeFormat</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.




## -see-also




<a href="https://msdn.microsoft.com/546cede1-1702-403a-bba3-b5cd3b35a1bf">GetDateFormat</a>



<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/4d63888e-4496-4315-ac87-bf60c54daa37">GetTimeFormatEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

