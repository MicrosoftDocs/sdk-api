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

# __MIDL_IBackgroundCopyJob2_0002 enumeration


## -description


The 
<b>BG_AUTH_SCHEME</b> enumeration defines the constant values that specify the authentication scheme to use when a proxy or server requests user authentication.


## -enum-fields




### -field BG_AUTH_SCHEME_BASIC

Basic is a scheme in which the user name and password are sent in clear-text to the server or proxy.


### -field BG_AUTH_SCHEME_DIGEST

Digest is a challenge-response scheme that uses a server-specified data string for the challenge.


### -field BG_AUTH_SCHEME_NTLM

NTLM is a challenge-response scheme that uses the credentials of the user for authentication in a Windows network environment.


### -field BG_AUTH_SCHEME_NEGOTIATE

Simple and Protected Negotiation protocol (Snego) is a challenge-response scheme that negotiates with the server or proxy to determine which scheme to use for authentication. Examples are the Kerberos protocol and  NTLM.


### -field BG_AUTH_SCHEME_PASSPORT

Passport is a centralized authentication service provided by Microsoft that offers a single logon for member sites.


## -remarks



BITS supports Passport authentication for explicit credentials only, not implicit credentials tied to the account.

The following table shows the   authentication requests that BITS does not support.

<table>
<tr>
<th>Scenario not supported</th>
<th>Windows Server 2003</th>
<th>Windows XP</th>
</tr>
<tr>
<td>Passport authentication on the server when the proxy requires authentication (using the HTTPS protocol).</td>
<td>Not supported</td>
<td>Not supported</td>
</tr>
<tr>
<td>Any authentication scheme on the server when the proxy requires Digest authentication.</td>
<td>Not supported</td>
<td>Not supported</td>
</tr>
<tr>
<td>Negotiate authentication on the server when the proxy requires Basic authentication.</td>
<td></td>
<td>Not supported</td>
</tr>
<tr>
<td>Using HTTPS when the proxy  requires Digest authentication.</td>
<td></td>
<td>Not supported</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt427474">Authentication</a>



<a href="https://msdn.microsoft.com/f89ebf46-da83-495c-bafe-b2e0f72f5d8e">BG_AUTH_CREDENTIALS</a>



<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a>
 

 

