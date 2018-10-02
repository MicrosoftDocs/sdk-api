---
UID: NC:davclnt.PFNDAVAUTHCALLBACK
title: PFNDAVAUTHCALLBACK
author: windows-sdk-content
description: The WebDAV client calls the application-defined DavAuthCallback callback function to prompt the user for credentials.
old-location: webdav\authcallback.htm
tech.root: WebDAV
ms.assetid: 6ac191ac-e63f-431f-893b-92c69320db58
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DAV_AUTHN_SCHEME_BASIC, DAV_AUTHN_SCHEME_CERT, DAV_AUTHN_SCHEME_DIGEST, DAV_AUTHN_SCHEME_FBA, DAV_AUTHN_SCHEME_NEGOTIATE, DAV_AUTHN_SCHEME_NTLM, DAV_AUTHN_SCHEME_PASSPORT, DavAuthCallback, DavAuthCallback callback function [WebDAV], PFNDAVAUTHCALLBACK, PFNDAVAUTHCALLBACK callback, davclnt/DavAuthCallback, webdav.authcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Davclnt.h
api_name:
 - DavAuthCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNDAVAUTHCALLBACK callback function


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

<a href="https://msdn.microsoft.com/35a38858-d36f-45c9-95f4-2541a182f5ac">Microsoft NTLM</a> authentication is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_PASSPORT"></a><a id="dav_authn_scheme_passport"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_PASSPORT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">

<a href="http.passport">Passport authentication</a> is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_DIGEST"></a><a id="dav_authn_scheme_digest"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_DIGEST</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/c65bb134-d480-4a71-872c-30e2884237a6">Microsoft Digest authentication</a> is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="DAV_AUTHN_SCHEME_NEGOTIATE"></a><a id="dav_authn_scheme_negotiate"></a><dl>
<dt><b>DAV_AUTHN_SCHEME_NEGOTIATE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a> is to be used.

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

The flags that the WebDAV service passed in the <i>dwFlags</i> parameter when it called the <a href="https://msdn.microsoft.com/b0d730f7-595e-4ea7-8688-db479dcc40b4">NPAddConnection3</a> function.


### -param pCallbackCred [in, out]

A pointer to a <a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a> structure.


### -param *NextStep [in, out]

A pointer to an  <a href="https://msdn.microsoft.com/e9ce9e61-c395-4f6b-843c-c1caa13ac3b4">AUTHNEXTSTEP</a> enumeration value that specifies the next action that the WebDAV client should take after  a successful call to the <i>DavAuthCallback</i> callback function.


### -param *pFreeCred [out]

A pointer to a <a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a> callback function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The <i>DavAuthCallback</i> callback function must be registered by calling the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.

To unregister this callback function, use the <a href="https://msdn.microsoft.com/5277d9ce-22e6-49d5-9a9c-c02993605bdf">DavUnregisterAuthCallback</a> function.

This callback function should prompt the user for credentials (either a <a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">user name and password</a> or an <a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">authentication BLOB</a>) and store this information in the appropriate member of the <a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a> structure that the <i>pCallbackCred</i> parameter points to.




## -see-also




<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a>



<a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a>



<a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a>



<a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a>



<a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a>
 

 

