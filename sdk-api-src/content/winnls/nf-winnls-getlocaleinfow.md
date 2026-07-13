---
UID: NF:winnls.GetLocaleInfoW
title: GetLocaleInfoW function (winnls.h)
description: Retrieves information about a locale specified by identifier. (Unicode)
helpviewer_keywords: ["GetLocaleInfo", "GetLocaleInfo function [Internationalization for Windows Applications]", "GetLocaleInfoW", "_win32_GetLocaleInfo", "intl.getlocaleinfo", "winnls/GetLocaleInfo", "winnls/GetLocaleInfoW"]
old-location: intl\getlocaleinfo.htm
tech.root: Intl
ms.assetid: 091b3f17-ccf7-493c-8992-00425f37d0ec
ms.date: 12/05/2018
ms.keywords: GetLocaleInfo, GetLocaleInfo function [Internationalization for Windows Applications], GetLocaleInfoA, GetLocaleInfoW, _win32_GetLocaleInfo, intl.getlocaleinfo, winnls/GetLocaleInfo, winnls/GetLocaleInfoA, winnls/GetLocaleInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLocaleInfoW (Unicode) and GetLocaleInfoA (ANSI)
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
 - GetLocaleInfoW
 - winnls/GetLocaleInfoW
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
 - GetLocaleInfo
 - GetLocaleInfoA
 - GetLocaleInfoW
---

# GetLocaleInfoW function


## -description

Retrieves information about a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a> function to <b>GetLocaleInfo</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> for which to retrieve information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>

### -param LCType [in]

The locale information to retrieve. For detailed definitions, see the <i>LCType</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>.

<div class="alert"><b>Note</b>  For <b>GetLocaleInfo</b>, the value LOCALE_USE_CP_ACP is relevant only for the ANSI version.</div>
<div> </div>

### -param lpLCData [out, optional]

Pointer to a buffer in which this function retrieves the requested locale information. This pointer is not used if <i>cchData</i> is set to 0. For more information, see the Remarks section.

### -param cchData [in]

Size, in TCHAR values, of the data buffer indicated by <i>lpLCData</i>. Alternatively, the application can set this parameter to 0. In this case, the function does not use the <i>lpLCData</i> parameter and returns the required buffer size, including the terminating null character.

## -returns

Returns the number of characters retrieved in the locale data buffer if successful and <i>cchData</i> is a nonzero value. If the function succeeds, <i>cchData</i> is nonzero, and <a href="/windows/desktop/Intl/locale-return-constants">LOCALE_RETURN_NUMBER</a> is specified, the return value is the size of the integer retrieved in the data buffer; that is, 2 for the Unicode version of the function or 4 for the ANSI version. If the function succeeds and the value of <i>cchData</i> is 0, the return value is the required size, in characters including a null character, for the locale data buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

For the operation of this function, see Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>.

<div class="alert"><b>Note</b>   Even when the <i>LCType</i> parameter is specified as LOCALE_FONTSIGNATURE, <i>cchData</i> and the function return are still TCHAR counts. The count is different for the ANSI and Unicode versions of the function. When an application calls the generic version of <b>GetLocaleInfo</b> with LOCALE_FONTSIGNATURE, <i>cchData</i> can be safely specified as sizeof(LOCALESIGNATURE) / sizeof(TCHAR).</div>
<div> </div>
The following examples deal correctly with the buffer size for non-text values:


```cpp
int   ret;
CALID calid;
DWORD value;

ret = GetLocaleInfo(LOCALE_USER_DEFAULT,
                    LOCALE_ICALENDARTYPE | LOCALE_RETURN_NUMBER,
                    (LPTSTR)&value,
                    sizeof(value) / sizeof(TCHAR) );
calid = value;

LOCALESIGNATURE LocSig;

ret = GetLocaleInfo(LOCALE_USER_DEFAULT,
                    LOCALE_FONTSIGNATURE,
                    (LPWSTR)&LocSig,
                    sizeof(LocSig) / sizeof(TCHAR) );

```


The ANSI string retrieved by the ANSI version of this function is translated from Unicode to ANSI based on the default ANSI code page for the locale identifier. However, if <a href="/windows/desktop/Intl/locale-use-cp-acp">LOCALE_USE_CP_ACP</a> is specified, the translation is based on the system default ANSI code page.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      





> [!NOTE]
> The winnls.h header defines GetLocaleInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/retrieving-and-setting-locale-information">Retrieving and Setting Locale Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setlocaleinfoa">SetLocaleInfo</a>
