---
UID: NF:wininet.InternetSetFilePointer
title: InternetSetFilePointer function (wininet.h)
description: Sets a file position for InternetReadFile. This is a synchronous call; however, subsequent calls to InternetReadFile might block or return pending if the data is not available from the cache and the server does not support random access.
helpviewer_keywords: ["InternetSetFilePointer","InternetSetFilePointer function [WinINet]","_inet_internetsetfilepointer_function","wininet.internetsetfilepointer","wininet/InternetSetFilePointer"]
old-location: wininet\internetsetfilepointer.htm
tech.root: wininet
ms.assetid: 0fdd85cb-f6a9-4a08-b72b-10d2075efb59
ms.date: 12/05/2018
ms.keywords: InternetSetFilePointer, InternetSetFilePointer function [WinINet], _inet_internetsetfilepointer_function, wininet.internetsetfilepointer, wininet/InternetSetFilePointer
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - InternetSetFilePointer
 - wininet/InternetSetFilePointer
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
 - InternetSetFilePointer
---

# InternetSetFilePointer function


## -description

Sets a file position for 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a>. This is a synchronous call; however, subsequent calls to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a> might block or return pending if the data is not available from the cache and the server does not support random access.

## -parameters

### -param hFile [in]

Handle returned from a previous call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> (on an HTTP or HTTPS
						URL) or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> (using the GET or HEAD HTTP verb and passed to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>). This handle must not have been created with the 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_DONT_CACHE</a> or 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_NO_CACHE_WRITE</a> value set.

### -param lDistanceToMove [in]

The low order 32-bits of a signed 64-bit number of bytes to move the file pointer. <b>Internet Explorer 7 and earlier:  </b><b>InternetSetFilePointer</b> used to move the pointer only within the bounds of  a LONG. When calling this older version of the function, <i>lpDistanceToMoveHigh</i> is reserved and should be set to <b>0</b>. A positive value moves the pointer forward in the file; a negative value moves it backward.

### -param lpDistanceToMoveHigh [in, out]

A pointer to the high order 32-bits of the signed 64-bit distance to move. If you do not need the high order 32-bits, this pointer must  be set to <b>NULL</b>.  When not <b>NULL</b>, this parameter also receives the high order DWORD of the new value of the file pointer. A positive value moves the pointer forward in the file; a negative value moves it backward.<b>Internet Explorer 7 and earlier:  </b><b>InternetSetFilePointer</b> used to move the pointer only within the bounds of  a LONG. When calling this older version of the function, <i>lpDistanceToMoveHigh</i> is reserved and should be set to <b>0</b>.

### -param dwMoveMethod [in]

Starting point for the file pointer move. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FILE_BEGIN</dt>
</dl>
</td>
<td width="60%">
Starting point is zero or the beginning of the file. If FILE_BEGIN is specified, 
<i>lDistanceToMove</i> is interpreted as an unsigned location for the new file pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FILE_CURRENT</dt>
</dl>
</td>
<td width="60%">
Current value of the file pointer is the starting point.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FILE_END</dt>
</dl>
</td>
<td width="60%">
Current end-of-file position is the starting point. This method fails if the content length is unknown.

</td>
</tr>
</table>

### -param dwContext [in]

This parameter is reserved and must be 0.

## -returns

I the function succeeds, it returns the current file position.     A return value of <b>INVALID_SET_FILE_POINTER</b> indicates a potential failure and needs to be followed by be a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.  

Since <b>INVALID_SET_FILE_POINTER</b> is a valid value for the  low-order DWORD of the new file pointer, the caller must check both the
return value of the function and the error code returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine whether or not an error has occurred.   If an error has occurred, the return value of InternetSetFilePointer        is <b>INVALID_SET_FILE_POINTER</b> and <b>GetLastError</b> returns a value other than <b>NO_ERROR</b>.

If the function succeeds and <i>lpDistanceToMoveHigh</i> is <b>NULL</b>, the return value is the low-order <b>DWORD</b> of the new file pointer.

Note that if the function returns a value other than <b>INVALID_SET_FILE_POINTER</b>, the call to <b>InternetSetFilePointer</b> has succeeded and there is no need to call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the function succeeds and <i>lpDistanceToMoveHigh</i> is not <b>NULL</b>, the return value is the lower-order <b>DWORD</b> of the new file pointer and <i>lpDistanceToMoveHigh</i> contains the high order <b>DWORD</b> of the new file pointer.

If a new file pointer is a negative value, the function fails, the file pointer is not moved, and the code returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is <b>ERROR_NEGATIVE_SEEK</b>.

If <i>lpDistanceToMoveHigh</i> is <b>NULL</b> and the new file position does not fit in a 32-bit value the function fails and returns <b>INVALID_SET_FILE_POINTER</b>.

## -remarks

This function cannot be used once the end of the file has been reached by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a>.

For 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handles created by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> and sent by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>, a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpendrequesta">HttpEndRequest</a> must be made on the handle before 
<b>InternetSetFilePointer</b> is used.

<b>InternetSetFilePointer</b> cannot be used reliably if the content length is unknown.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<b>InternetSetFilePointer</b> has changed over time. In Internet Explorer 7 and earlier, it  used to move the pointer only within the bounds of  a LONG. When calling this older version of the function, <i>lDistanceToMove</i> contains the entire value. A positive value moves the pointer forward in the file; a negative value moves it backward.  <i>lpDistanceToMoveHigh</i> is reserved and is set to <b>0</b>.  In current versions, <i>lpDistanceToMoveHigh</i> is a significant value and where any negative value would be indicated.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>