---
UID: NF:wininet.InternetQueryOptionW
title: InternetQueryOptionW function (wininet.h)
description: Queries an Internet option on the specified handle. (Unicode)
helpviewer_keywords: ["InternetQueryOption", "InternetQueryOption function [WinINet]", "InternetQueryOptionW", "_inet_internetqueryoption_function", "wininet.internetqueryoption", "wininet/InternetQueryOption", "wininet/InternetQueryOptionW"]
old-location: wininet\internetqueryoption.htm
tech.root: wininet
ms.assetid: b0bafd3d-8f54-429e-b423-dae3d61b0030
ms.date: 12/05/2018
ms.keywords: InternetQueryOption, InternetQueryOption function [WinINet], InternetQueryOptionA, InternetQueryOptionW, _inet_internetqueryoption_function, wininet.internetqueryoption, wininet/InternetQueryOption, wininet/InternetQueryOptionA, wininet/InternetQueryOptionW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetQueryOptionW (Unicode) and InternetQueryOptionA (ANSI)
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
 - InternetQueryOptionW
 - wininet/InternetQueryOptionW
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
 - InternetQueryOption
 - InternetQueryOptionA
 - InternetQueryOptionW
---

# InternetQueryOptionW function


## -description

Queries an Internet option on the specified handle.

## -parameters

### -param hInternet [in]

Handle on which to query information.

### -param dwOption [in]

Internet option to be queried. This can be one of the 
<a href="/windows/desktop/WinInet/option-flags">Option Flags</a> values.

### -param lpBuffer [out]

Pointer to a buffer that receives the option setting. Strings returned by 
<b>InternetQueryOption</b> are globally allocated, so the calling application must  free them when it  is finished using them.

### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the size of 
<i>lpBuffer</i>, in bytes.  When 
<b>InternetQueryOption</b> returns, 
<i>lpdwBufferLength</i> specifies the size of the data placed into 
<i>lpBuffer</i>. If 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter points to the number of bytes required to hold the requested information.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return the <b>ERROR_INVALID_PARAMETER</b> if an option flag that is invalid for the specified handle type is passed to the 
<i>dwOption</i> parameter.

For more  information, see  
<a href="/windows/desktop/WinInet/setting-and-retrieving-internet-options">Setting and Retrieving Internet Options</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetQueryOption as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpgetfilea">FtpGetFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpputfilea">FtpPutFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
