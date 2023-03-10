---
UID: NF:winhttp.WinHttpSetOption
title: WinHttpSetOption function (winhttp.h)
description: The WinHttpSetOption function sets an Internet option.
helpviewer_keywords: ["WinHttpSetOption","WinHttpSetOption function [WinHTTP]","http.winhttpsetoption","winhttp.winhttpsetoption_function","winhttp/WinHttpSetOption"]
old-location: http\winhttpsetoption.htm
tech.root: http
ms.assetid: bcf1da09-5787-4d2a-82ae-6965e27fa477
ms.date: 12/05/2018
ms.keywords: WinHttpSetOption, WinHttpSetOption function [WinHTTP], http.winhttpsetoption, winhttp.winhttpsetoption_function, winhttp/WinHttpSetOption
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpSetOption
 - winhttp/WinHttpSetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpSetOption
---

# WinHttpSetOption function


## -description

The <b>WinHttpSetOption</b> function sets an Internet option.

## -parameters

### -param hInternet [in]

The <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle on which to set data. Be aware  that this can be either a Session handle or a Request handle, depending on what option is being set. For more information about how to determine which handle is appropriate to use in setting a particular option, see the  <a href="/windows/desktop/WinHttp/option-flags">Option Flags</a>.

### -param dwOption [in]

An unsigned long integer value that contains the Internet option to set. This can be one of the 
<a href="/windows/desktop/WinHttp/option-flags">Option Flags</a> values.

### -param lpBuffer [in]

A pointer to a buffer that contains the option setting.

### -param dwBufferLength [in]

Unsigned long integer value that contains the length of the 
<i>lpBuffer</i> buffer. The length of the buffer is specified in characters for the following options; for all other options, the length is specified in bytes.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following:

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be carried out because the handle supplied is not in the correct state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_OPTION</b></dt>
</dl>
</td>
<td width="60%">
A request to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> or 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> specified an invalid option value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid.

This value will be returned if <b>WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL</b> is set to a value lower than 15000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPTION_NOT_SETTABLE</b></dt>
</dl>
</td>
<td width="60%">
The requested option cannot be set, only queried.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid.

This value will be returned if <b>WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL</b> is set to a value lower than 15000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

Credentials passed to <b>WinHttpSetOption</b> could be unexpectedly sent in plaintext. It is  strongly recommended that you  use <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryauthschemes">WinHttpQueryAuthSchemes</a>  and <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetcredentials">WinHttpSetCredentials</a> instead of <b>WinHttpSetOption</b> for setting credentials.

<div class="alert"><b>Note</b>  When using Passport authentication, however, a WinHTTP application responding to a 407 status code must use <b>WinHttpSetOption</b> to provide proxy credentials rather than <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetcredentials">WinHttpSetCredentials</a>. This is only true when using Passport authentication; in all other circumstances,  use <b>WinHttpSetCredentials</b>.</div>
<div> </div>
Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the error ERROR_INVALID_PARAMETER if an option flag is specified that cannot be set.

For more information and code examples that show the use of <b>WinHttpSetOption</b>, see <a href="/windows/desktop/WinHttp/authentication-in-winhttp">Authentication in WinHTTP</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/authentication-in-winhttp">Authentication in WinHTTP</a>



<a href="/windows/desktop/WinHttp/option-flags">Option Flags</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a>