---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IKEEXT_KERBEROS_AUTHENTICATION1__ structure


## -description


The <b>IKEEXT_KERBEROS_AUTHENTICATION1</b> structure contains information needed for preshared key authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_KERBEROS_AUTHENTICATION1</b> is the specific implementation of IKEEXT_KERBEROS_AUTHENTICATION used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/2dd626c2-4b70-450a-ad6a-a978f1d93bbf">IKEEXT_KERBEROS_AUTHENTICATION0</a> is available.</div><div> </div>

## -struct-fields




### -field flags

Type: <b>UINT32</b>

A combination of the following values.

<table>
<tr>
<th>Kerberos authentication flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION"></a><a id="ikeext_kerb_auth_disable_initiator_token_generation"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION</b></dt>
</dl>
</td>
<td width="60%">
Disable initiator generation of peer token from the peer's name string.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS"></a><a id="ikeext_kerb_auth_dont_accept_explicit_credentials"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Refuse connections if the peer is using explicit credentials.

Applicable only to  AuthIP.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_FORCE_PROXY_ON_INITIATOR_"></a><a id="ikeext_kerb_auth_force_proxy_on_initiator_"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_FORCE_PROXY_ON_INITIATOR </b></dt>
</dl>
</td>
<td width="60%">
Force the use of a Kerberos proxy server when acting as initiator.

</td>
</tr>
</table>
 


### -field proxyServer

Type: <b>wchar_t*</b>

The Kerberos proxy server.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

