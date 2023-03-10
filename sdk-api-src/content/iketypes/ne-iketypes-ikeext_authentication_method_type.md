---
UID: NE:iketypes.IKEEXT_AUTHENTICATION_METHOD_TYPE_
title: IKEEXT_AUTHENTICATION_METHOD_TYPE (iketypes.h)
description: Specifies the type of authentication method used by Internet Key Exchange (IKE), Authenticated Internet Protocol (AuthIP), or IKEv2.
helpviewer_keywords: ["IKEEXT_ANONYMOUS","IKEEXT_AUTHENTICATION_METHOD_TYPE","IKEEXT_AUTHENTICATION_METHOD_TYPE enumeration [Filtering]","IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX","IKEEXT_CERTIFICATE","IKEEXT_CERTIFICATE_ECDSA_P256","IKEEXT_CERTIFICATE_ECDSA_P384","IKEEXT_EAP","IKEEXT_IPV6_CGA","IKEEXT_KERBEROS","IKEEXT_NTLM_V2","IKEEXT_PRESHARED_KEY","IKEEXT_RESERVED","IKEEXT_SSL","IKEEXT_SSL_ECDSA_P256","IKEEXT_SSL_ECDSA_P384","fwp.ikeext_authentication_method_type","iketypes/IKEEXT_ANONYMOUS","iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE","iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX","iketypes/IKEEXT_CERTIFICATE","iketypes/IKEEXT_CERTIFICATE_ECDSA_P256","iketypes/IKEEXT_CERTIFICATE_ECDSA_P384","iketypes/IKEEXT_EAP","iketypes/IKEEXT_IPV6_CGA","iketypes/IKEEXT_KERBEROS","iketypes/IKEEXT_NTLM_V2","iketypes/IKEEXT_PRESHARED_KEY","iketypes/IKEEXT_RESERVED","iketypes/IKEEXT_SSL","iketypes/IKEEXT_SSL_ECDSA_P256","iketypes/IKEEXT_SSL_ECDSA_P384"]
old-location: fwp\ikeext_authentication_method_type.htm
tech.root: fwp
ms.assetid: 582ec1ea-9390-4f86-9a3c-25d4e805a218
ms.date: 12/05/2018
ms.keywords: IKEEXT_ANONYMOUS, IKEEXT_AUTHENTICATION_METHOD_TYPE, IKEEXT_AUTHENTICATION_METHOD_TYPE enumeration [Filtering], IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX, IKEEXT_CERTIFICATE, IKEEXT_CERTIFICATE_ECDSA_P256, IKEEXT_CERTIFICATE_ECDSA_P384, IKEEXT_EAP, IKEEXT_IPV6_CGA, IKEEXT_KERBEROS, IKEEXT_NTLM_V2, IKEEXT_PRESHARED_KEY, IKEEXT_RESERVED, IKEEXT_SSL, IKEEXT_SSL_ECDSA_P256, IKEEXT_SSL_ECDSA_P384, fwp.ikeext_authentication_method_type, iketypes/IKEEXT_ANONYMOUS, iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE, iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX, iketypes/IKEEXT_CERTIFICATE, iketypes/IKEEXT_CERTIFICATE_ECDSA_P256, iketypes/IKEEXT_CERTIFICATE_ECDSA_P384, iketypes/IKEEXT_EAP, iketypes/IKEEXT_IPV6_CGA, iketypes/IKEEXT_KERBEROS, iketypes/IKEEXT_NTLM_V2, iketypes/IKEEXT_PRESHARED_KEY, iketypes/IKEEXT_RESERVED, iketypes/IKEEXT_SSL, iketypes/IKEEXT_SSL_ECDSA_P256, iketypes/IKEEXT_SSL_ECDSA_P384
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_AUTHENTICATION_METHOD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_AUTHENTICATION_METHOD_TYPE_
 - iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE_
 - IKEEXT_AUTHENTICATION_METHOD_TYPE
 - iketypes/IKEEXT_AUTHENTICATION_METHOD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_AUTHENTICATION_METHOD_TYPE
---

# IKEEXT_AUTHENTICATION_METHOD_TYPE enumeration


## -description

The <b>IKEEXT_AUTHENTICATION_METHOD_TYPE</b> enumerated type specifies the type of authentication method used by Internet Key Exchange (IKE), Authenticated Internet Protocol (AuthIP), or IKEv2..

## -enum-fields

### -field IKEEXT_PRESHARED_KEY:0

Specifies pre-shared key authentication method. Available only for IKE.

### -field IKEEXT_CERTIFICATE

Specifies certificate authentication method. Available only for IKE and IKEv2.

### -field IKEEXT_KERBEROS

Specifies Kerberos authentication method.

### -field IKEEXT_ANONYMOUS

Specifies anonymous authentication method. Available only for AuthIP.

### -field IKEEXT_SSL

Specifies Secure Sockets Layer (SSL) authentication method. Available only for AuthIP.

### -field IKEEXT_NTLM_V2

Specifies Microsoft Windows NT LAN Manager (NTLM) V2 authentication method. Available only for AuthIP.

### -field IKEEXT_IPV6_CGA

Specifies IPv6 Cryptographically Generated Addresses (CGA) authentication method. Available only for IKE.

### -field IKEEXT_CERTIFICATE_ECDSA_P256

Specifies Elliptic Curve Digital Signature Algorithm (ECDSA) 256 certificate authentication method. Available only for IKE and IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_CERTIFICATE_ECDSA_P384

Specifies ECDSA-384 certificate authentication method. Available only for IKE and IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_SSL_ECDSA_P256

Specifies ECDSA-256 SSL authentication method. Available only for AuthIP.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_SSL_ECDSA_P384

Specifies ECDSA-384 SSL authentication method. Available only for AuthIP.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_EAP

Specifies Extensible Authentication Protocol (EAP) authentication method. Available only for IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field IKEEXT_RESERVED

Reserved. Do not use.

<div class="alert"><b>Note</b>  Available only on Windows Server 2012, Windows 8, and later.</div>
<div> </div>

### -field IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
