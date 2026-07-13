---
UID: NF:wininet.InternetSetOptionA
title: InternetSetOptionA function (wininet.h)
description: Sets an Internet option. (ANSI)
helpviewer_keywords: ["InternetSetOptionA", "wininet/InternetSetOptionA"]
old-location: wininet\internetsetoption.htm
tech.root: wininet
ms.assetid: 578c7130-7426-4a2e-ae0f-ed8a84449b06
ms.date: 12/05/2018
ms.keywords: InternetSetOption, InternetSetOption function [WinINet], InternetSetOptionA, InternetSetOptionW, _inet_internetsetoption_function, wininet.internetsetoption, wininet/InternetSetOption, wininet/InternetSetOptionA, wininet/InternetSetOptionW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetOptionW (Unicode) and InternetSetOptionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetSetOptionA
 - wininet/InternetSetOptionA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetOption
 - InternetSetOptionA
 - InternetSetOptionW
---

# InternetSetOptionA function


## -description

Sets an Internet option.

## -parameters

### -param hInternet [in]

Handle on which to set information.

### -param dwOption [in]

Internet option to be set. This can be one of the 
<a href="/windows/desktop/WinInet/option-flags">Option Flags</a> values.

### -param lpBuffer [in]

Pointer to a buffer that contains the option setting.

### -param dwBufferLength [in]

Size of the 
<i>lpBuffer</i> buffer.  If 
<i>lpBuffer</i> contains a string, 
the size is in <b>TCHARs</b>.  If 
<i>lpBuffer</i> contains anything other than a string, 
the size is in bytes.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return the error <b>ERROR_INVALID_PARAMETER</b> if an option flag that cannot be set is specified.

For more information, see 
<a href="/windows/desktop/WinInet/setting-and-retrieving-internet-options">Setting and Retrieving Internet Options</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetSetOption as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpgetfilea">FtpGetFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpputfilea">FtpPutFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
