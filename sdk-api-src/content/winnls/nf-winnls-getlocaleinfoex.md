---
UID: NF:winnls.GetLocaleInfoEx
title: GetLocaleInfoEx function (winnls.h)
description: Retrieves information about a locale specified by name.Note  The application should call this function in preference to GetLocaleInfo if designed to run only on Windows Vista and later. Note  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["GetLocaleInfoEx","GetLocaleInfoEx function [Internationalization for Windows Applications]","_win32_GetLocaleInfoEx","intl.getlocaleinfoex","winnls/GetLocaleInfoEx"]
old-location: intl\getlocaleinfoex.htm
tech.root: Intl
ms.assetid: 20294ff2-b783-41a2-92a8-41cd974a2ccb
ms.date: 12/05/2018
ms.keywords: GetLocaleInfoEx, GetLocaleInfoEx function [Internationalization for Windows Applications], _win32_GetLocaleInfoEx, intl.getlocaleinfoex, winnls/GetLocaleInfoEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetLocaleInfoEx
 - winnls/GetLocaleInfoEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetLocaleInfoEx
---

# GetLocaleInfoEx function


## -description

Retrieves information about a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>

## -parameters

### -param lpLocaleName [in, optional]

Pointer to a <a href="/windows/desktop/Intl/locale-names">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param LCType [in]

The locale information to retrieve. For possible values, see the "Constants Used in the LCType Parameter of GetLocaleInfo, GetLocaleInfoEx, and SetLocaleInfo" section in <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>. Note that only one piece of locale information can be specified per call. 

The application can use the binary OR operator to combine <a href="/windows/desktop/Intl/locale-return-constants">LOCALE_RETURN_NUMBER</a> with any other allowed constant. In this case, the function retrieves the value as a number instead of a string. The buffer that receives the value must be at least the length of a DWORD value, which is 2.

<div class="alert"><b>Caution</b>  It is also possible to combine <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> with any other constant. However, use of this constant is strongly discouraged. (Even without using the current user override, the data can differ from computer to computer, and custom locales can change the data. For example, even month or day names are subject to spelling reforms.)</div>
<div> </div>
If <i>LCType</i> is set to <a href="/windows/desktop/Intl/locale-ioptionalcalendar">LOCALE_IOPTIONALCALENDAR</a>, the function retrieves only the first alternate calendar. 

<div class="alert"><b>Note</b>  To get all alternate calendars, the application should use <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a>.</div>
<div> </div>
Starting with Windows Vista, your applications should not use <a href="/windows/desktop/Intl/locale-ilanguage">LOCALE_ILANGUAGE</a> in the <i>LCType</i> parameter to avoid failure or retrieval of unexpected data. Instead, it is recommended for your applications to call <b>GetLocaleInfoEx</b>.

### -param lpLCData [out, optional]

Pointer to a buffer in which this function retrieves the requested locale information. This pointer is not used if <i>cchData</i> is set to 0.

### -param cchData [in]

Size, in characters, of the data buffer indicated by <i>lpLCData</i>. Alternatively, the application can set this parameter to 0. In this case, the function does not use the <i>lpLCData</i> parameter and returns the required buffer size, including the terminating null character.

## -returns

Returns the number of characters retrieved in the locale data buffer if successful and <i>cchData</i> is a nonzero value. If the function succeeds, <i>cchData</i> is nonzero, and <a href="/windows/desktop/Intl/locale-return-constants">LOCALE_RETURN_NUMBER</a> is specified, the return value is the size of the integer retrieved in the data buffer, that is, 2. If the function succeeds and the value of <i>cchData</i> is 0, the return value is the required size, in characters including a null character, for the locale data buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function normally retrieves information in text format. If the information is a numeric value and the value of <i>LCType</i> is <a href="/windows/desktop/Intl/locale-ilanguage">LOCALE_ILANGUAGE</a> or <a href="/windows/desktop/Intl/locale-idefault-constants">LOCALE_IDEFAULTLANGUAGE</a>, this function retrieves strings containing hexadecimal numbers. Otherwise, the retrieved text for numeric information is a decimal number.

There are two exceptions to this rule. First, the application can retrieve numeric values as integers by specifying <a href="/windows/desktop/Intl/locale-return-constants">LOCALE_RETURN_NUMBER</a> in the <i>LCType</i> parameter. The second exception is that <a href="/windows/desktop/Intl/locale-fontsignature">LOCALE_FONTSIGNATURE</a> behaves differently from all other locale information constants. The application must provide a data buffer of at least sizeof(LOCALESIGNATURE) bytes. On successful return from the function, the buffer is filled in as a <a href="/windows/desktop/api/wingdi/ns-wingdi-localesignature">LOCALESIGNATURE</a> structure.

<div class="alert"><b>Note</b>  Even when the <i>LCType</i> parameter is specified as LOCALE_FONTSIGNATURE, <i>cchData</i> and the function return are still character counts. When an application calls <b>GetLocaleInfoEx</b> with <i>LCType</i> specified as LOCALE_FONTSIGNATURE, <i>cchData</i> can be safely specified as sizeof(LOCALESIGNATURE) / sizeof(WCHAR).</div>
<div> </div>
The following examples deal correctly with the buffer size for non-text values:


```cpp
int   ret;
CALID calid;
DWORD value;

ret = GetLocaleInfoEx(LOCALE_NAME_USER_DEFAULT,
                      LOCALE_ICALENDARTYPE | LOCALE_RETURN_NUMBER,
                      (LPWSTR)&value,
                      sizeof(value) / sizeof(WCHAR) );
calid = value;

LOCALESIGNATURE LocSig;

ret = GetLocaleInfoEx(LOCALE_NAME_USER_DEFAULT,
                      LOCALE_FONTSIGNATURE,
                      (LPWSTR)&LocSig,
                      sizeof(LocSig) / sizeof(WCHAR) );

```


This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.


#### Examples

Examples showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a> and <a href="/windows/desktop/Intl/nls--internationalized-domain-name--idn--mitigation-sample">NLS: Internationalized Domain Name (IDN) Mitigation Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/retrieving-and-setting-locale-information">Retrieving and Setting Locale Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setlocaleinfoa">SetLocaleInfo</a>