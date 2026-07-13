---
UID: NF:winineti.InternetGoOnlineA
title: InternetGoOnlineA function (winineti.h)
description: The InternetGoOnlineA (ANSI) function (winineti.h) prompts the user for permission to initiate connection to a URL.
helpviewer_keywords: ["INTERNET_GOONLINE_REFRESH", "InternetGoOnlineA", "winineti/InternetGoOnlineA"]
old-location: wininet\internetgoonline.htm
tech.root: wininet
ms.assetid: ed1c0282-5469-49d5-8a8c-b7671d27ebd2
ms.date: 08/15/2022
ms.keywords: INTERNET_GOONLINE_REFRESH, InternetGoOnline, InternetGoOnline function [WinINet], InternetGoOnlineA, InternetGoOnlineW, _inet_internetgoonline_function, wininet.internetgoonline, winineti/InternetGoOnline, winineti/InternetGoOnlineA, winineti/InternetGoOnlineW
req.header: winineti.h
req.include-header: Wininet.h, Winineti.h, Wininet.h, Winineti.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGoOnlineW (Unicode) and InternetGoOnlineA (ANSI)
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
 - InternetGoOnlineA
 - winineti/InternetGoOnlineA
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
 - InternetGoOnline
 - InternetGoOnlineA
 - InternetGoOnlineW
---

# InternetGoOnlineA function


## -description

Prompts the user for permission to initiate connection to a URL.

## -parameters

### -param lpszURL [in]

Pointer to a null-terminated string that specifies the URL of the website for the connection.

### -param hwndParent [in]

Handle to the parent window.

### -param dwFlags [in]

This parameter can be zero or the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_GOONLINE_REFRESH"></a><a id="internet_goonline_refresh"></a><dl>
<dt><b>INTERNET_GOONLINE_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. Applications can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to retrieve the error code.

If the functions fails, it can  return the following error code:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is incorrect.

The <i>dwFlags</i> parameter contains a value other than zero or <b>INTERNET_GOONLINE_REFRESH</b>.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The winineti.h header defines InternetGoOnline as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/establishing-a-dial-up-connection-to-the-internet">Establishing a Dial-Up Connection to the Internet</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
