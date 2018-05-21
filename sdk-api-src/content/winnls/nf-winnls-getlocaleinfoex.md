---
UID: NF:winnls.GetLocaleInfoEx
title: GetLocaleInfoEx function
author: windows-driver-content
description: Retrieves information about a locale specified by name.Note  The application should call this function in preference to GetLocaleInfo if designed to run only on Windows Vista and later. Note  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
old-location: intl\getlocaleinfoex.htm
old-project: Intl
ms.assetid: 20294ff2-b783-41a2-92a8-41cd974a2ccb
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetLocaleInfoEx, GetLocaleInfoEx function [Internationalization for Windows Applications], _win32_GetLocaleInfoEx, intl.getlocaleinfoex, winnls/GetLocaleInfoEx
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
-	API-MS-Win-Core-Localization-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-l1-2-0.dll
-	API-MS-Win-Core-Localization-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
-	GetLocaleInfoEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetLocaleInfoEx function


## -description


Retrieves information about a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a> if designed to run only on Windows Vista and later.</div>
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

### -param LCType [in]

The locale information to retrieve. For possible values, see the "Constants Used in the LCType Parameter of GetLocaleInfo, GetLocaleInfoEx, and SetLocaleInfo" section in <a href="https://msdn.microsoft.com/45798dd1-34bb-4e99-8f84-94f28e76711f">Locale Information Constants</a>. Note that only one piece of locale information can be specified per call. 

The application can use the binary OR operator to combine <a href="https://msdn.microsoft.com/c6aadf84-c597-4cbd-a715-b68325ce5117">LOCALE_RETURN_NUMBER</a> with any other allowed constant. In this case, the function retrieves the value as a number instead of a string. The buffer that receives the value must be at least the length of a DWORD value, which is 2.

<div class="alert"><b>Caution</b>  It is also possible to combine <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> with any other constant. However, use of this constant is strongly discouraged. (Even without using the current user override, the data can differ from computer to computer, and custom locales can change the data. For example, even month or day names are subject to spelling reforms.)</div>
<div> </div>
If <i>LCType</i> is set to <a href="https://msdn.microsoft.com/a944bdfc-6c07-4e78-b4d2-a26d66f18327">LOCALE_IOPTIONALCALENDAR</a>, the function retrieves only the first alternate calendar. 

<div class="alert"><b>Note</b>  To get all alternate calendars, the application should use <a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a>.</div>
<div> </div>

            Starting with Windows Vista, your applications should not use <a href="https://msdn.microsoft.com/8f80a941-8ba6-4a0d-92fa-77230fe0a9d1">LOCALE_ILANGUAGE</a> in the <i>LCType</i> parameter to avoid failure or retrieval of unexpected data. Instead, it is recommended for your applications to call <b>GetLocaleInfoEx</b>.


### -param lpLCData [out, optional]

Pointer to a buffer in which this function retrieves the requested locale information. This pointer is not used if <i>cchData</i> is set to 0.


### -param cchData [in]

Size, in characters, of the data buffer indicated by <i>lpLCData</i>. Alternatively, the application can set this parameter to 0. In this case, the function does not use the <i>lpLCData</i> parameter and returns the required buffer size, including the terminating null character.


## -returns



Returns the number of characters retrieved in the locale data buffer if successful and <i>cchData</i> is a nonzero value. If the function succeeds, <i>cchData</i> is nonzero, and <a href="https://msdn.microsoft.com/c6aadf84-c597-4cbd-a715-b68325ce5117">LOCALE_RETURN_NUMBER</a> is specified, the return value is the size of the integer retrieved in the data buffer, that is, 2. If the function succeeds and the value of <i>cchData</i> is 0, the return value is the required size, in characters including a null character, for the locale data buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function normally retrieves information in text format. If the information is a numeric value and the value of <i>LCType</i> is <a href="https://msdn.microsoft.com/8f80a941-8ba6-4a0d-92fa-77230fe0a9d1">LOCALE_ILANGUAGE</a> or <a href="https://msdn.microsoft.com/4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361">LOCALE_IDEFAULTLANGUAGE</a>, this function retrieves strings containing hexadecimal numbers. Otherwise, the retrieved text for numeric information is a decimal number.

There are two exceptions to this rule. First, the application can retrieve numeric values as integers by specifying <a href="https://msdn.microsoft.com/c6aadf84-c597-4cbd-a715-b68325ce5117">LOCALE_RETURN_NUMBER</a> in the <i>LCType</i> parameter. The second exception is that <a href="https://msdn.microsoft.com/95f3f0ef-07ca-4fbc-9c5f-6db15fc4c68a">LOCALE_FONTSIGNATURE</a> behaves differently from all other locale information constants. The application must provide a data buffer of at least sizeof(LOCALESIGNATURE) bytes. On successful return from the function, the buffer is filled in as a <a href="https://msdn.microsoft.com/54510d73-f2a2-4176-8080-cdf855e99217">LOCALESIGNATURE</a> structure.

<div class="alert"><b>Note</b>  Even when the <i>LCType</i> parameter is specified as LOCALE_FONTSIGNATURE, <i>cchData</i> and the function return are still character counts. When an application calls <b>GetLocaleInfoEx</b> with <i>LCType</i> specified as LOCALE_FONTSIGNATURE, <i>cchData</i> can be safely specified as sizeof(LOCALESIGNATURE) / sizeof(WCHAR).</div>
<div> </div>
The following examples deal correctly with the buffer size for non-text values:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>int   ret;
CALID calid;
DWORD value;

ret = GetLocaleInfoEx(LOCALE_NAME_USER_DEFAULT,
                      LOCALE_ICALENDARTYPE | LOCALE_RETURN_NUMBER,
                      (LPWSTR)&amp;value,
                      sizeof(value) / sizeof(WCHAR) );
calid = value;

LOCALESIGNATURE LocSig;

ret = GetLocaleInfoEx(LOCALE_NAME_USER_DEFAULT,
                      LOCALE_FONTSIGNATURE,
                      (LPWSTR)&amp;LocSig,
                      sizeof(LocSig) / sizeof(WCHAR) );
</pre>
</td>
</tr>
</table></span></div>
This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.


#### Examples

Examples showing the use of this function can be found in <a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a> and <a href="https://msdn.microsoft.com/73a96129-5234-4c70-b36a-baa5cb4daa0a">NLS: Internationalized Domain Name (IDN) Mitigation Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/091b3f17-ccf7-493c-8992-00425f37d0ec">GetLocaleInfo</a>



<a href="https://msdn.microsoft.com/1e925e41-64db-44aa-ab73-05d0f2036c8f">GetSystemDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/81b896de-1f06-4315-aa64-90806c0fed75">GetUserDefaultLocaleName</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/7675f826-76be-4361-a82c-9573040a7e72">Retrieving and Setting Locale Information</a>



<a href="https://msdn.microsoft.com/96e031cb-0d9f-4556-b9b3-3451d8f80da5">SetLocaleInfo</a>
 

 

