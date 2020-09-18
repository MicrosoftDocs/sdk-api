---
UID: NF:winnls.EnumDateFormatsExEx
title: EnumDateFormatsExEx function (winnls.h)
description: Enumerates the long date, short date, or year/month formats that are available for a locale specified by name.Note  The application should call this function in preference to EnumDateFormats or EnumDateFormatsEx if designed to run only on Windows Vista and later. Note  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["DATE_LONGDATE","DATE_MONTHDAY","DATE_SHORTDATE","DATE_YEARMONTH","EnumDateFormatsExEx","EnumDateFormatsExEx function [Internationalization for Windows Applications]","_win32_EnumDateFormatsExEx","intl.enumdateformatsexex","winnls/EnumDateFormatsExEx"]
old-location: intl\enumdateformatsexex.htm
tech.root: Intl
ms.assetid: 52bfec03-4cb3-4418-b467-f75d2900ba40
ms.date: 12/05/2018
ms.keywords: DATE_LONGDATE, DATE_MONTHDAY, DATE_SHORTDATE, DATE_YEARMONTH, EnumDateFormatsExEx, EnumDateFormatsExEx function [Internationalization for Windows Applications], _win32_EnumDateFormatsExEx, intl.enumdateformatsexex, winnls/EnumDateFormatsExEx
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
 - EnumDateFormatsExEx
 - winnls/EnumDateFormatsExEx
dev_langs:
 - c++
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
 - EnumDateFormatsExEx
---

# EnumDateFormatsExEx function


## -description

Enumerates the long date, short date, or year/month formats that are available for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a> or <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>

## -parameters

### -param lpDateFmtEnumProcExEx [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317815(v=vs.85)">EnumDateFormatsProcExEx</a>.

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

### -param dwFlags [in]

Flag specifying date formats. The application can supply one of the following values or the <a href="/windows/desktop/Intl/locale-use-cp-acp">LOCALE_USE_CP_ACP</a> constant.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DATE_SHORTDATE"></a><a id="date_shortdate"></a><dl>
<dt><b>DATE_SHORTDATE</b></dt>
</dl>
</td>
<td width="60%">
Use short date formats. This value cannot be used with any of the other flag values.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_LONGDATE"></a><a id="date_longdate"></a><dl>
<dt><b>DATE_LONGDATE</b></dt>
</dl>
</td>
<td width="60%">
Use long date formats. This value cannot be used with any of the other flag values.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_YEARMONTH"></a><a id="date_yearmonth"></a><dl>
<dt><b>DATE_YEARMONTH</b></dt>
</dl>
</td>
<td width="60%">
Use year/month formats. This value cannot be used with any of the other flag values.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_MONTHDAY"></a><a id="date_monthday"></a><dl>
<dt><b>DATE_MONTHDAY</b></dt>
</dl>
</td>
<td width="60%">
Use month/day formats. This value cannot be used with any of the other flag values.

</td>
</tr>
</table>

### -param lParam [in]

An application-provided parameter to pass to the callback function. This value is especially useful for multi-threaded applications.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="/windows/uwp/design/globalizing/japanese-era-change">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
The function enumerates the date formats by passing date format string pointers, one at a time, to the specified application-defined callback function, along with an application-defined constant that is useful for multi-threaded applications. This process continues until <b>EnumDateFormatsExEx</b> finds the last date format or the callback function returns <b>FALSE</b>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317815(v=vs.85)">EnumDateFormatsProcExEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>