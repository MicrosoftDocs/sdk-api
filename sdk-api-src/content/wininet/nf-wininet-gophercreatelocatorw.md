---
UID: NF:wininet.GopherCreateLocatorW
title: GopherCreateLocatorW function (wininet.h)
description: Creates a Gopher or Gopher+ locator string from the selector string's component parts. (Unicode)
helpviewer_keywords: ["GopherCreateLocator", "GopherCreateLocator function [WinINet]", "GopherCreateLocatorW", "_inet_gophercreatelocator_function", "wininet.gophercreatelocator", "wininet/GopherCreateLocator", "wininet/GopherCreateLocatorW"]
old-location: wininet\gophercreatelocator.htm
tech.root: wininet
ms.assetid: 972a4ff9-efda-4784-9ac8-c76e679e8032
ms.date: 12/05/2018
ms.keywords: GopherCreateLocator, GopherCreateLocator function [WinINet], GopherCreateLocatorA, GopherCreateLocatorW, _inet_gophercreatelocator_function, wininet.gophercreatelocator, wininet/GopherCreateLocator, wininet/GopherCreateLocatorA, wininet/GopherCreateLocatorW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherCreateLocatorW (Unicode) and GopherCreateLocatorA (ANSI)
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
 - GopherCreateLocatorW
 - wininet/GopherCreateLocatorW
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
 - GopherCreateLocator
 - GopherCreateLocatorA
 - GopherCreateLocatorW
---

# GopherCreateLocatorW function


## -description

<p class="CCE_Message">[The <b>GopherCreateLocator</b> function is available for use in the operating systems specified in the Requirements section.]

Creates a Gopher or Gopher+ locator string from the selector string's component parts.

## -parameters

### -param lpszHost [in]

Pointer to a <b>null</b>-terminated string that contains the name of the host, or a dotted-decimal IP address (such as 198.105.232.1).

### -param nServerPort [in]

Port number on which the Gopher server at 
<i>lpszHost</i> lives, in host byte order. If 
<i>nServerPort</i> is <b>INTERNET_INVALID_PORT_NUMBER</b>, the default Gopher port is used.

### -param lpszDisplayString [in]

Pointer to a <b>null</b>-terminated string that contains the Gopher document or directory to be displayed. If this parameter is <b>NULL</b>, the function returns the default directory for the Gopher server.

### -param lpszSelectorString [in]

Pointer to the selector string to send to the Gopher server in order to retrieve information. This parameter can be <b>NULL</b>.

### -param dwGopherType [in]

Determines whether 
<i>lpszSelectorString</i> refers to a directory or document, and whether the request is Gopher+ or Gopher. The default value, GOPHER_TYPE_DIRECTORY, is used if the value of 
<i>dwGopherType</i> is zero. This can be one of the 
<a href="/windows/desktop/WinInet/gopher-type-values">gopher type values</a>.

### -param lpszLocator [out]

Pointer to a buffer  that receives the locator string. If 
<i>lpszLocator</i> is <b>NULL</b>, 
<i>lpdwBufferLength</i> receives the necessary buffer length, but the function performs no other processing.

### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the length of the 
<i>lpszLocator</i> buffer, in characters. When the function returns, this parameter receives the number of characters written to the 
buffer. If 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>, this parameter receives the number of characters required.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a>.

## -remarks

To retrieve information from a Gopher server, an application must first get a Gopher "locator" from the Gopher server.

The locator, which the application should treat as an opaque token, is normally used for calls to the 
<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a> function to retrieve a specific piece of information.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GopherCreateLocator as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
