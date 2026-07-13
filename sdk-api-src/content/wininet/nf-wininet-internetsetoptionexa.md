---
UID: NF:wininet.InternetSetOptionExA
title: InternetSetOptionExA function (wininet.h)
description: Not supported.Implemented only as a stub that calls the InternetSetOption function; InternetSetOptionEx has no functionality of its own. Do not use this function at this time. (ANSI)
helpviewer_keywords: ["InternetSetOptionExA", "wininet/InternetSetOptionExA"]
old-location: wininet\internetsetoptionex.htm
tech.root: wininet
ms.assetid: 535e4f38-d941-4b69-8c48-ea47f3fbd5e7
ms.date: 12/05/2018
ms.keywords: InternetSetOptionEx, InternetSetOptionEx function [WinINet], InternetSetOptionExA, InternetSetOptionExW, _inet_internetsetoptionex_function, wininet.internetsetoptionex, wininet/InternetSetOptionEx, wininet/InternetSetOptionExA, wininet/InternetSetOptionExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetOptionExW (Unicode) and InternetSetOptionExA (ANSI)
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
 - InternetSetOptionExA
 - wininet/InternetSetOptionExA
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
 - InternetSetOptionEx
 - InternetSetOptionExA
 - InternetSetOptionExW
---

# InternetSetOptionExA function


## -description

Not supported.

Implemented only as a stub that calls the <a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a> function; <b>InternetSetOptionEx</b> has no functionality of its own. Do not use this function at this time.

## -parameters

### -param hInternet

Unused.

### -param dwOption

Unused.

### -param lpBuffer

Unused.

### -param dwBufferLength

Unused.

### -param dwFlags

Unused.

## -returns

This function does not return a value.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetSetOptionEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>
