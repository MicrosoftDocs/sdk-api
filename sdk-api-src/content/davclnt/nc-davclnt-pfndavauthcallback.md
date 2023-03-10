---
UID: NC:davclnt.PFNDAVAUTHCALLBACK
title: PFNDAVAUTHCALLBACK (davclnt.h)
description: The WebDAV client calls the application-defined DavAuthCallback callback function to prompt the user for credentials.
helpviewer_keywords: ["DAV_AUTHN_SCHEME_BASIC","DAV_AUTHN_SCHEME_CERT","DAV_AUTHN_SCHEME_DIGEST","DAV_AUTHN_SCHEME_FBA","DAV_AUTHN_SCHEME_NEGOTIATE","DAV_AUTHN_SCHEME_NTLM","DAV_AUTHN_SCHEME_PASSPORT","DavAuthCallback","DavAuthCallback callback function [WebDAV]","PFNDAVAUTHCALLBACK","PFNDAVAUTHCALLBACK callback","davclnt/DavAuthCallback","webdav.authcallback"]
old-location: webdav\authcallback.htm
tech.root: WebDAV
ms.assetid: 6ac191ac-e63f-431f-893b-92c69320db58
ms.date: 12/05/2018
ms.keywords: DAV_AUTHN_SCHEME_BASIC, DAV_AUTHN_SCHEME_CERT, DAV_AUTHN_SCHEME_DIGEST, DAV_AUTHN_SCHEME_FBA, DAV_AUTHN_SCHEME_NEGOTIATE, DAV_AUTHN_SCHEME_NTLM, DAV_AUTHN_SCHEME_PASSPORT, DavAuthCallback, DavAuthCallback callback function [WebDAV], PFNDAVAUTHCALLBACK, PFNDAVAUTHCALLBACK callback, davclnt/DavAuthCallback, webdav.authcallback
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNDAVAUTHCALLBACK
 - davclnt/PFNDAVAUTHCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Davclnt.h
api_name:
 - DavAuthCallback
---

## -description

The WebDAV client calls the application-defined <i>DavAuthCallback</i> callback function to prompt the user for credentials.

The <i>PFNDAVAUTHCALLBACK</i> type defines a pointer to this callback function. <i>DavAuthCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param lpwzServerName [in]

A pointer to a <b>NULL</b>-terminated Unicode string that contains the name of the target server.

### -param lpwzRemoteName [in]

A pointer to a <b>NULL</b>-terminated Unicode string that contains the name of the network resource.

### -param dwAuthScheme [in]

A bitmask of flags that specify the authentication schemes to be used.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_BASIC"></a><a id="dav_authn_scheme_basic"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_BASIC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Basic authentication is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_NTLM"></a><a id="dav_authn_scheme_ntlm"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_NTLM</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecAuthN/microsoft-ntlm">Microsoft NTLM</a> authentication is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_PASSPORT"></a><a id="dav_authn_scheme_passport"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_PASSPORT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/WinHttp/passport-authentication-in-winhttp">Passport authentication</a> is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_DIGEST"></a><a id="dav_authn_scheme_digest"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_DIGEST</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecAuthN/microsoft-digest-authentication">Microsoft Digest authentication</a> is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_NEGOTIATE"></a><a id="dav_authn_scheme_negotiate"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_NEGOTIATE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a> is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_CERT"></a><a id="dav_authn_scheme_cert"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_CERT</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Certificate authentication is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_FBA"></a><a id="dav_authn_scheme_fba"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_FBA</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Forms-based authentication is to be used.

</td>
</tr>
</table>

### -param dwFlags [in]

The flags that the WebDAV service passed in the <i>dwFlags</i> parameter when it called the <a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection3">NPAddConnection3</a> function.

### -param pCallbackCred [in, out]

A pointer to a <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_cred">DAV_CALLBACK_CRED</a> structure.

### -param NextStep [in, out]

A pointer to an  <a href="/windows/desktop/api/davclnt/ne-davclnt-authnextstep">AUTHNEXTSTEP</a> enumeration value that specifies the next action that the WebDAV client should take after  a successful call to the <i>DavAuthCallback</i> callback function.

### -param pFreeCred [out]

A pointer to a <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback_freecred">DavFreeCredCallback</a> callback function.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <i>DavAuthCallback</i> callback function must be registered by calling the <a href="/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.

To unregister this callback function, use the <a href="/windows/desktop/api/davclnt/nf-davclnt-davunregisterauthcallback">DavUnregisterAuthCallback</a> function.

This callback function should prompt the user for credentials (either a <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_unp">user name and password</a> or an <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_blob">authentication BLOB</a>) and store this information in the appropriate member of the <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_cred">DAV_CALLBACK_CRED</a> structure that the <i>pCallbackCred</i> parameter points to.

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa">CredUIPromptForCredentials</a>



<a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a>



<a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_blob">DAV_CALLBACK_AUTH_BLOB</a>



<a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_unp">DAV_CALLBACK_AUTH_UNP</a>



<a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback_freecred">DavFreeCredCallback</a>