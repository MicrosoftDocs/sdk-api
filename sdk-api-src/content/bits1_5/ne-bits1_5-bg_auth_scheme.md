---
UID: NE:bits1_5.BG_AUTH_SCHEME
title: BG_AUTH_SCHEME
description: Defines constants that specify the authentication scheme to use when a proxy or server requests user authentication.
helpviewer_keywords: ["BG_AUTH_SCHEME","BG_AUTH_SCHEME enumeration [BITS]","BG_AUTH_SCHEME_BASIC","BG_AUTH_SCHEME_DIGEST","BG_AUTH_SCHEME_NEGOTIATE","BG_AUTH_SCHEME_NTLM","BG_AUTH_SCHEME_PASSPORT","_drz_bg_auth_scheme","bits.bg_auth_scheme","bits1_5/BG_AUTH_SCHEME","bits1_5/BG_AUTH_SCHEME_BASIC","bits1_5/BG_AUTH_SCHEME_DIGEST","bits1_5/BG_AUTH_SCHEME_NEGOTIATE","bits1_5/BG_AUTH_SCHEME_NTLM","bits1_5/BG_AUTH_SCHEME_PASSPORT"]
old-location: bits\bg_auth_scheme.htm
tech.root: Bits
ms.assetid: e5a97cee-0012-4e30-850a-9adc258a36d3
ms.date: 02/20/2019
ms.keywords: BG_AUTH_SCHEME, BG_AUTH_SCHEME enumeration [BITS], BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_NTLM, BG_AUTH_SCHEME_PASSPORT, _drz_bg_auth_scheme, bits.bg_auth_scheme, bits1_5/BG_AUTH_SCHEME, bits1_5/BG_AUTH_SCHEME_BASIC, bits1_5/BG_AUTH_SCHEME_DIGEST, bits1_5/BG_AUTH_SCHEME_NEGOTIATE, bits1_5/BG_AUTH_SCHEME_NTLM, bits1_5/BG_AUTH_SCHEME_PASSPORT
req.header: bits1_5.h
req.include-header: Bits.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_AUTH_SCHEME
req.redist: BITS 1.5 on Windows XP
f1_keywords:
 - BG_AUTH_SCHEME
 - bits1_5/BG_AUTH_SCHEME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_AUTH_SCHEME
---

# BG_AUTH_SCHEME enumeration


## -description

Defines constants that specify the authentication scheme to use when a proxy or server requests user authentication.

## -enum-fields

### -field BG_AUTH_SCHEME_BASIC:1

<em>Basic</em> is a scheme in which the user name and password are sent in clear-text to the server or proxy.

### -field BG_AUTH_SCHEME_DIGEST

<em>Digest</em> is a challenge-response scheme that uses a server-specified data string for the challenge.

### -field BG_AUTH_SCHEME_NTLM

<em>NTLM</em> is a challenge-response scheme that uses the credentials of the user for authentication in a Windows network environment.

### -field BG_AUTH_SCHEME_NEGOTIATE

<em>Simple and Protected Negotiation</em> (Snego) is a challenge-response scheme that negotiates with the server or proxy to determine which scheme to use for authentication. Examples are the Kerberos protocol, and NTLM.

### -field BG_AUTH_SCHEME_PASSPORT

<em>Passport</em> is a centralized authentication service provided by Microsoft that offers a single logon for member sites.

## -remarks

BITS supports Passport authentication for explicit credentials only, not implicit credentials tied to the account.

The following table shows the authentication requests that BITS does not support.

|Scenario|Windows XP|Windows Server 2003|
|-|-|-|
|Passport authentication on the server when the proxy requires authentication (using the HTTPS protocol).|Not supported|Not supported|
|Any authentication scheme on the server when the proxy requires Digest authentication.|Not supported|Not supported|
|Negotiate authentication on the server when the proxy requires Basic authentication.|Not supported||
|Using HTTPS when the proxy requires Digest authentication.|Not supported||

## -see-also

* [Authentication](/windows/desktop/Bits/authentication)
* [BG_AUTH_CREDENTIALS structure](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials)
* [IBackgroundCopyJob2::SetCredentials method](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)

