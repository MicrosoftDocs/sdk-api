---
UID: NF:winnls.GetGeoInfoW
title: GetGeoInfoW function (winnls.h)
description: Retrieves information about a specified geographical location. (Unicode)
helpviewer_keywords: ["GetGeoInfo", "GetGeoInfo function [Internationalization for Windows Applications]", "GetGeoInfoW", "_win32_GetGeoInfo", "intl.getgeoinfo", "winnls/GetGeoInfo", "winnls/GetGeoInfoW"]
old-location: intl\getgeoinfo.htm
tech.root: Intl
ms.assetid: 73827ed9-bdc5-4b34-b849-fb44b3c5bd6e
ms.date: 12/05/2018
ms.keywords: GetGeoInfo, GetGeoInfo function [Internationalization for Windows Applications], GetGeoInfoA, GetGeoInfoW, _win32_GetGeoInfo, intl.getgeoinfo, winnls/GetGeoInfo, winnls/GetGeoInfoA, winnls/GetGeoInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetGeoInfoW (Unicode) and GetGeoInfoA (ANSI)
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
 - GetGeoInfoW
 - winnls/GetGeoInfoW
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetGeoInfo
 - GetGeoInfoA
 - GetGeoInfoW
---

# GetGeoInfoW function


## -description

<p class="CCE_Message">[<b>GetGeoInfo</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a>.

]

Retrieves information about a specified geographical location.

## -parameters

### -param Location [in]

Identifier for the geographical location for which to get information. For more information, see <a href="/windows/desktop/Intl/table-of-geographical-locations">Table of Geographical Locations</a>. You can obtain the available values by calling <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemgeoid">EnumSystemGeoID</a>.

### -param GeoType [in]

Type of information to retrieve. Possible values are defined by the <a href="/windows/desktop/api/winnls/ne-winnls-sysgeotype">SYSGEOTYPE</a> enumeration. If the value of <i>GeoType</i> is GEO_LCID, the function retrieves a locale identifier. If the value of <i>GeoType</i> is GEO_RFC1766, the function retrieves a string name that is compliant with RFC 4646 (Windows Vista). For more information, see the Remarks section.

<b>Windows XP:</b> When <i>GeoType</i> is set to GEO_LCID, the retrieved string is an 8-digit hexadecimal value.

<b>Windows Me:</b> When <i>GeoType</i> is set to GEO_LCID, the retrieved string is a decimal value.

### -param lpGeoData [out, optional]

Pointer to the buffer in which this function retrieves the information.

### -param cchData [in]

Size of the buffer indicated by <i>lpGeoData</i>. The size is the number of bytes for the ANSI version of the function, or the number of words for the Unicode version. The application can set this parameter to 0 if the function is to return the required size of the buffer.

### -param LangId [in]

Identifier for the language, used with the value of <i>Location</i>. The application can set this parameter to 0, with GEO_RFC1766 or GEO_LCID specified for <i>GeoType</i>. This setting causes the function to retrieve the language identifier by calling <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlangid">GetUserDefaultLangID</a>.

<div class="alert"><b>Note</b>   The application must set this parameter to 0 if <i>GeoType</i> has any value other than GEO_RFC1766 or GEO_LCID.</div>
<div> </div>

## -returns

Returns the number of bytes (ANSI) or words (Unicode) of geographical location information retrieved in the output buffer. If <i>cchData</i> is set to 0, the function returns the required size for the buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

If the application specifies GEO_RFC1766 for <i>GeoType</i>, it should specify a language identifier for <i>LangId</i> that is appropriate to the specified geographical location identifier. The appropriate language is either a locale-neutral language or one with a locale corresponding to the specified identifier. The resulting string, compliant with RFC 4646 (Windows Vista), constitutes a <a href="/windows/desktop/Intl/locale-names">locale name</a>.

For example, if <i>Location</i> is specified as 0xF4 for United States, <i>GeoType</i> is specified as GEO_RFC1766, and <i>LangId</i> is specified as either 0x09 for locale-neutral English or 0x409 for English (United States), the function retrieves "en-US" on successful return. In fact, the function ignores the locale-specific portion of the language. Thus, if the application specifies <i>LangId</i> as 0x809 for English (United Kingdom), the function also writes "en-US" to <i>lpGeoData</i>.

Consider another example. If <i>Location</i> is specified as 0xF4 for United States, <i>GeoType</i> is specified as GEO_RFC1766, and <i>LangId</i> is specified as 0x04 for Chinese, the function retrieves "zh-US" on successful return. This is not the name of a supported locale.

If the application specifies GEO_LCID for <i>GeoType</i>, the function treats the language identifier as a locale identifier (LCID). It attempts to return the locale identifier if it is associated with the provided geographical identifier in some way. 





> [!NOTE]
> The winnls.h header defines GetGeoInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemgeoid">EnumSystemGeoID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getgeoinfoex">GetGeoInfoEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/ne-winnls-sysgeotype">SYSGEOTYPE</a>
