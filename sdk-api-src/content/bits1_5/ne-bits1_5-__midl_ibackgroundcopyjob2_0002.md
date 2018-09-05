---
UID: NE:bits1_5.__MIDL_IBackgroundCopyJob2_0002
title: "__MIDL_IBackgroundCopyJob2_0002"
author: windows-sdk-content
description: The BG_AUTH_SCHEME enumeration defines the constant values that specify the authentication scheme to use when a proxy or server requests user authentication.
old-location: bits\bg_auth_scheme.htm
old-project: bits
ms.assetid: e5a97cee-0012-4e30-850a-9adc258a36d3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_AUTH_SCHEME, BG_AUTH_SCHEME enumeration [BITS], BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_NTLM, BG_AUTH_SCHEME_PASSPORT, __MIDL_IBackgroundCopyJob2_0002, _drz_bg_auth_scheme, bits.bg_auth_scheme, bits1_5/BG_AUTH_SCHEME, bits1_5/BG_AUTH_SCHEME_BASIC, bits1_5/BG_AUTH_SCHEME_DIGEST, bits1_5/BG_AUTH_SCHEME_NEGOTIATE, bits1_5/BG_AUTH_SCHEME_NTLM, bits1_5/BG_AUTH_SCHEME_PASSPORT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: bits1_5.h
req.include-header: Bits.h
req.redist: BITS 1.5 on  Windows XP
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_AUTH_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_AUTH_SCHEME
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/cfd4aec3-79d0-4971-93f8-df797e5c0f75">Authentication</a>



<a href="https://msdn.microsoft.com/f89ebf46-da83-495c-bafe-b2e0f72f5d8e">BG_AUTH_CREDENTIALS</a>



<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a>
 

 

