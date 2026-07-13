---
UID: NF:wininet.InternetGetLastResponseInfoA
title: InternetGetLastResponseInfoA function (wininet.h)
description: Retrieves the last error description or server response on the thread calling this function. (ANSI)
helpviewer_keywords: ["InternetGetLastResponseInfoA", "wininet/InternetGetLastResponseInfoA"]
old-location: wininet\internetgetlastresponseinfo.htm
tech.root: wininet
ms.assetid: 0aa274c5-0aa0-4eb9-8aef-3128e735759d
ms.date: 12/05/2018
ms.keywords: InternetGetLastResponseInfo, InternetGetLastResponseInfo function [WinINet], InternetGetLastResponseInfoA, InternetGetLastResponseInfoW, _win32_internetgetlastresponseinfo, wininet.internetgetlastresponseinfo, wininet/InternetGetLastResponseInfo, wininet/InternetGetLastResponseInfoA, wininet/InternetGetLastResponseInfoW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetLastResponseInfoW (Unicode) and InternetGetLastResponseInfoA (ANSI)
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
 - InternetGetLastResponseInfoA
 - wininet/InternetGetLastResponseInfoA
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
 - InternetGetLastResponseInfo
 - InternetGetLastResponseInfoA
 - InternetGetLastResponseInfoW
---

# InternetGetLastResponseInfoA function


## -description

Retrieves the last error description or server response on the thread calling this function.

## -parameters

### -param lpdwError [out]

Pointer to a variable that receives an error message pertaining to the operation that failed.

### -param lpszBuffer [out]

Pointer to a buffer that receives the error text.

### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the size of the 
<i>lpszBuffer</i> buffer, in <b>TCHARs</b>. When the function returns, this parameter contains the size of the string written to the buffer, not including the terminating zero.

## -returns

Returns <b>TRUE</b> if error text was successfully written to the buffer, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the buffer is too small to hold all the error text, 
<b>GetLastError</b> returns <b>ERROR_INSUFFICIENT_BUFFER</b>, and the 
<i>lpdwBufferLength</i> parameter contains the minimum buffer size required to return all the error text.

## -remarks

The FTP protocols can return additional text information along with most errors. This extended error information can be retrieved by using the 
<b>InternetGetLastResponseInfo</b> function whenever 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
<a href="/windows/desktop/WinInet/wininet-errors">ERROR_INTERNET_EXTENDED_ERROR</a> (occurring after an unsuccessful function call).

The buffer pointed to by 
<i>lpszBuffer</i> must be large enough to hold both the error string and a zero terminator at the end of the string. However, note that the value returned in 
<i>lpdwBufferLength</i> does not include the terminating zero.

<b>InternetGetLastResponseInfo</b> can be called multiple times until another function is called on this thread. When another function is called, the internal buffer that is storing the last response information is cleared.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetGetLastResponseInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
