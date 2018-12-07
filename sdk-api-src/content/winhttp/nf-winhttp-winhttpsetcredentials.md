---
UID: NF:winhttp.WinHttpSetCredentials
title: WinHttpSetCredentials function
author: windows-sdk-content
description: The WinHttpSetCredentials function passes the required authorization credentials to the server.
old-location: http\winhttpsetcredentials.htm
tech.root: WinHttp
ms.assetid: a864c708-9481-460a-87aa-1d31c344c0a1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WINHTTP_AUTH_SCHEME_BASIC, WINHTTP_AUTH_SCHEME_DIGEST, WINHTTP_AUTH_SCHEME_NEGOTIATE, WINHTTP_AUTH_SCHEME_NTLM, WINHTTP_AUTH_SCHEME_PASSPORT, WINHTTP_AUTH_TARGET_PROXY, WINHTTP_AUTH_TARGET_SERVER, WinHttpSetCredentials, WinHttpSetCredentials function [WinHTTP], http.winhttpsetcredentials, winhttp.winhttpsetcredentials_function, winhttp/WinHttpSetCredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpSetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
---

# WinHttpSetCredentials function


## -description


The <b>WinHttpSetCredentials</b> function passes the required authorization credentials to the server.


## -parameters




### -param hRequest [in]

Valid 
<a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle returned by 
<a href="https://msdn.microsoft.com/9ecd035d-1abf-48ca-baf2-d9754f912c60">WinHttpOpenRequest</a>.


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
<a href="https://msdn.microsoft.com/37fb9342-c5c2-46a3-a8b0-83060aa997e2">WinHttpQueryAuthSchemes</a>. The following table identifies the possible values.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following table identifies the error codes returned.

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



Even when  WinHTTP is  used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The credentials set by <b>WinHttpSetCredentials</b> are only used for a single request; WinHTTP does not cache these credentials for use in subsequent requests. As a result, applications must be written so that they can respond to multiple challenges. If an authenticated connection is re-used, subsequent requests cannot be challenged, but your code should be able to respond to a challenge at any point.

For sample code that illustrates the use of <b>WinHttpSetCredentials</b>, see <a href="https://msdn.microsoft.com/077d6275-8600-4091-b78e-419a41a2101a">Authentication in WinHTTP</a>.

<div class="alert"><b>Note</b>  When using Passport authentication and responding to a 407 status code, a WinHTTP application must use <a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> to provide proxy credentials rather than <b>WinHttpSetCredentials</b>. This is only true when using Passport authentication; in all other circumstances,  use <b>WinHttpSetCredentials</b>, because <b>WinHttpSetOption</b>  is less secure.</div>
<div> </div>
<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/077d6275-8600-4091-b78e-419a41a2101a">Authentication in WinHTTP</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>



<a href="https://msdn.microsoft.com/afcdad8d-687e-4a1f-99d8-5d8be13825fa">WinHttpConnect</a>



<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>



<a href="https://msdn.microsoft.com/9ecd035d-1abf-48ca-baf2-d9754f912c60">WinHttpOpenRequest</a>



<a href="https://msdn.microsoft.com/37fb9342-c5c2-46a3-a8b0-83060aa997e2">WinHttpQueryAuthSchemes</a>
 

 

