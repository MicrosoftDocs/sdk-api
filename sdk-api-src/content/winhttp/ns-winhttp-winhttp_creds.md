---
UID: NS:winhttp.tagWINHTTP_CREDS
title: WINHTTP_CREDS (winhttp.h)
description: Contains user credential information used for server and proxy authentication. (WINHTTP_CREDS)
helpviewer_keywords: ["*PWINHTTP_CREDS","INHTTP_AUTH_SCHEME_DIGEST","PWINHTTP_CREDS","PWINHTTP_CREDS structure pointer [HTTP]","WINHTTP_AUTH_SCHEME_BASIC","WINHTTP_AUTH_SCHEME_NEGOTIATE","WINHTTP_AUTH_SCHEME_NTLM","WINHTTP_CREDS","WINHTTP_CREDS structure [HTTP]","http.winhttp_creds","winhttp/PWINHTTP_CREDS","winhttp/WINHTTP_CREDS"]
old-location: http\winhttp_creds.htm
tech.root: http
ms.assetid: dc4960b6-ca78-4b7d-a012-61fb7b0b1ef2
ms.date: 12/05/2018
ms.keywords: '*PWINHTTP_CREDS, INHTTP_AUTH_SCHEME_DIGEST, PWINHTTP_CREDS, PWINHTTP_CREDS structure pointer [HTTP], WINHTTP_AUTH_SCHEME_BASIC, WINHTTP_AUTH_SCHEME_NEGOTIATE, WINHTTP_AUTH_SCHEME_NTLM, WINHTTP_CREDS, WINHTTP_CREDS structure [HTTP], http.winhttp_creds, winhttp/PWINHTTP_CREDS, winhttp/WINHTTP_CREDS'
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINHTTP_CREDS, *PWINHTTP_CREDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWINHTTP_CREDS
 - winhttp/tagWINHTTP_CREDS
 - PWINHTTP_CREDS
 - winhttp/PWINHTTP_CREDS
 - WINHTTP_CREDS
 - winhttp/WINHTTP_CREDS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_CREDS
---

# WINHTTP_CREDS structure


## -description

The <b>WINHTTP_CREDS</b> structure contains user credential information used for server and proxy authentication.
<div class="alert"><b>Note</b>  This structure has been deprecated. Instead, the use of the <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_creds_ex">WINHTTP_CREDS_EX</a> structure is recommended.</div><div> </div>

## -struct-fields

### -field lpszUserName

Pointer to a buffer that contains username.

### -field lpszPassword

Pointer to a buffer that contains password.

### -field lpszRealm

Pointer to a buffer that contains realm.

### -field dwAuthScheme

A flag that contains the authentication scheme, as one of the following values.

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
<td width="40%"><a id="INHTTP_AUTH_SCHEME_DIGEST"></a><a id="inhttp_auth_scheme_digest"></a><dl>
<dt><b>INHTTP_AUTH_SCHEME_DIGEST</b></dt>
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
Select between NTLM and Kerberos authentication.

</td>
</tr>
</table>

### -field lpszHostName

 Pointer to a buffer that contains hostname.

### -field dwPort

The server connection port.

## -remarks

This structure is used with options <b>WINHTTP_OPTION_GLOBAL_SERVER_CREDS</b> and <b>WINHTTP_OPTION_GLOBAL_PROXY_CREDS</b>
<a href="/windows/desktop/WinHttp/option-flags">option flags</a>. These options require the registry key <b>HKLM\Software\Microsoft\Windows\CurrentVersion\Internet Settings!ShareCredsWithWinHttp</b>. This registry key is not present by default.

When it is set, WinINet will send credentials  down to WinHTTP. Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet. In order to share server credentials in addition to proxy credentials, users needs to set  the <b>WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS</b> option flag.

## -see-also

<a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_creds_ex">WINHTTP_CREDS_EX</a>
