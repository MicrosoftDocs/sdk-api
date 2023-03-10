---
UID: NF:winhttp.WinHttpSetCredentials
title: WinHttpSetCredentials function (winhttp.h)
description: The WinHttpSetCredentials function passes the required authorization credentials to the server.
helpviewer_keywords: ["WINHTTP_AUTH_SCHEME_BASIC","WINHTTP_AUTH_SCHEME_DIGEST","WINHTTP_AUTH_SCHEME_NEGOTIATE","WINHTTP_AUTH_SCHEME_NTLM","WINHTTP_AUTH_SCHEME_PASSPORT","WINHTTP_AUTH_TARGET_PROXY","WINHTTP_AUTH_TARGET_SERVER","WinHttpSetCredentials","WinHttpSetCredentials function [WinHTTP]","http.winhttpsetcredentials","winhttp.winhttpsetcredentials_function","winhttp/WinHttpSetCredentials"]
old-location: http\winhttpsetcredentials.htm
tech.root: http
ms.assetid: a864c708-9481-460a-87aa-1d31c344c0a1
ms.date: 12/05/2018
ms.keywords: WINHTTP_AUTH_SCHEME_BASIC, WINHTTP_AUTH_SCHEME_DIGEST, WINHTTP_AUTH_SCHEME_NEGOTIATE, WINHTTP_AUTH_SCHEME_NTLM, WINHTTP_AUTH_SCHEME_PASSPORT, WINHTTP_AUTH_TARGET_PROXY, WINHTTP_AUTH_TARGET_SERVER, WinHttpSetCredentials, WinHttpSetCredentials function [WinHTTP], http.winhttpsetcredentials, winhttp.winhttpsetcredentials_function, winhttp/WinHttpSetCredentials
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
 - WinHttpSetCredentials
 - winhttp/WinHttpSetCredentials
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
 - WinHttpSetCredentials
---

# WinHttpSetCredentials function


## -description

The <b>WinHttpSetCredentials</b> function passes the required authorization credentials to the server.

## -parameters

### -param hRequest [in]

Valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>.

### -param AuthTargets [in]

An unsigned integer that specifies a flag that contains the authentication target.  Can be one of the  values in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_TARGET_SERVER"></a><a id="winhttp_auth_target_server"></a><dl>
<dt><b>WINHTTP_AUTH_TARGET_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Credentials are passed to a server.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_TARGET_PROXY"></a><a id="winhttp_auth_target_proxy"></a><dl>
<dt><b>WINHTTP_AUTH_TARGET_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Credentials are passed to a proxy.

</td>
</tr>
</table>

### -param AuthScheme [in]

An unsigned integer that specifies a flag that contains the authentication scheme.  Must be one of the supported authentication schemes returned from 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryauthschemes">WinHttpQueryAuthSchemes</a>. The following table identifies the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_BASIC"></a><a id="winhttp_auth_scheme_basic"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Use basic authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NTLM"></a><a id="winhttp_auth_scheme_ntlm"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NTLM</b></dt>
</dl>
</td>
<td width="60%">
Use NTLM authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_PASSPORT"></a><a id="winhttp_auth_scheme_passport"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_PASSPORT</b></dt>
</dl>
</td>
<td width="60%">
Use passport authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_DIGEST"></a><a id="winhttp_auth_scheme_digest"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Use digest authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NEGOTIATE"></a><a id="winhttp_auth_scheme_negotiate"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
Selects between NTLM and Kerberos authentication.

</td>
</tr>
</table>

### -param pwszUserName [in]

Pointer to a string that contains a valid user name.

### -param pwszPassword [in]

Pointer to a string that contains a valid password.  The password can be blank.

### -param pAuthParams [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table identifies the error codes returned.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation (Windows error code).

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is  used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The credentials set by <b>WinHttpSetCredentials</b> are only used for a single request; WinHTTP does not cache these credentials for use in subsequent requests. As a result, applications must be written so that they can respond to multiple challenges. If an authenticated connection is re-used, subsequent requests cannot be challenged, but your code should be able to respond to a challenge at any point.

For sample code that illustrates the use of <b>WinHttpSetCredentials</b>, see <a href="/windows/desktop/WinHttp/authentication-in-winhttp">Authentication in WinHTTP</a>.

<div class="alert"><b>Note</b>  When using Passport authentication and responding to a 407 status code, a WinHTTP application must use <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> to provide proxy credentials rather than <b>WinHttpSetCredentials</b>. This is only true when using Passport authentication; in all other circumstances,  use <b>WinHttpSetCredentials</b>, because <b>WinHttpSetOption</b>  is less secure.</div>
<div> </div>
<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/authentication-in-winhttp">Authentication in WinHTTP</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryauthschemes">WinHttpQueryAuthSchemes</a>