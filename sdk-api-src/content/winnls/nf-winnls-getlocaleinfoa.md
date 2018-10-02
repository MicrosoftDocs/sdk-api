---
UID: NF:winnls.GetLocaleInfoA
title: GetLocaleInfoA function
author: windows-sdk-content
description: Retrieves information about a locale specified by identifier.
old-location: intl\getlocaleinfo.htm
tech.root: Intl
ms.assetid: 091b3f17-ccf7-493c-8992-00425f37d0ec
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetLocaleInfo, GetLocaleInfo function [Internationalization for Windows Applications], GetLocaleInfoA, GetLocaleInfoW, _win32_GetLocaleInfo, intl.getlocaleinfo, winnls/GetLocaleInfo, winnls/GetLocaleInfoA, winnls/GetLocaleInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - GetLocaleInfo
 - GetLocaleInfoA
 - GetLocaleInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLocaleInfoA function


## -description


Retrieves information about a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a> function to <b>GetLocaleInfo</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> for which to retrieve information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param LCType [in]

The locale information to retrieve. For detailed definitions, see the <i>LCType</i> parameter of <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>.

<div class="alert"><b>Note</b>  For <b>GetLocaleInfo</b>, the value LOCALE_USE_CP_ACP is relevant only for the ANSI version.</div>
<div> </div>

### -param lpLCData [out, optional]

Pointer to a buffer in which this function retrieves the requested locale information. This pointer is not used if <i>cchData</i> is set to 0. For more information, see the Remarks section.


### -param cchData [in]

Size, in TCHAR values, of the data buffer indicated by <i>lpLCData</i>. Alternatively, the application can set this parameter to 0. In this case, the function does not use the <i>lpLCData</i> parameter and returns the required buffer size, including the terminating null character.


## -returns



Returns the number of characters retrieved in the locale data buffer if successful and <i>cchData</i> is a nonzero value. If the function succeeds, <i>cchData</i> is nonzero, and <a href="https://msdn.microsoft.com/c6aadf84-c597-4cbd-a715-b68325ce5117">LOCALE_RETURN_NUMBER</a> is specified, the return value is the size of the integer retrieved in the data buffer; that is, 2 for the Unicode version of the function or 4 for the ANSI version. If the function succeeds and the value of <i>cchData</i> is 0, the return value is the required size, in characters including a null character, for the locale data buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



For the operation of this function, see Remarks for <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>.

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


The ANSI string retrieved by the ANSI version of this function is translated from Unicode to ANSI based on the default ANSI code page for the locale identifier. However, if <a href="https://msdn.microsoft.com/686ca9f2-515d-449f-8871-77c78ab5c31a">LOCALE_USE_CP_ACP</a> is specified, the translation is based on the system default ANSI code page.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      




## -see-also




<a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a>



<a href="https://msdn.microsoft.com/67d73d88-6a6c-439b-a321-1b1bd05fe268">GetSystemDefaultLCID</a>



<a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/7675f826-76be-4361-a82c-9573040a7e72">Retrieving and Setting Locale Information</a>



<a href="https://msdn.microsoft.com/96e031cb-0d9f-4556-b9b3-3451d8f80da5">SetLocaleInfo</a>
 

 

