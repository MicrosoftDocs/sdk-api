---
UID: NS:iketypes.IKEEXT_AUTHENTICATION_METHOD2_
title: IKEEXT_AUTHENTICATION_METHOD2 (iketypes.h)
description: Specifies various parameters for IKE/Authip authentication. (IKEEXT_AUTHENTICATION_METHOD2)
helpviewer_keywords: ["IKEEXT_AUTHENTICATION_METHOD2","IKEEXT_AUTHENTICATION_METHOD2 structure [Filtering]","fwp.ikeext_authentication_method2","iketypes/IKEEXT_AUTHENTICATION_METHOD2"]
old-location: fwp\ikeext_authentication_method2.htm
tech.root: fwp
ms.assetid: f0bd649e-746d-4802-87fe-d8baec2b252f
ms.date: 12/05/2018
ms.keywords: IKEEXT_AUTHENTICATION_METHOD2, IKEEXT_AUTHENTICATION_METHOD2 structure [Filtering], fwp.ikeext_authentication_method2, iketypes/IKEEXT_AUTHENTICATION_METHOD2
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEEXT_AUTHENTICATION_METHOD2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_AUTHENTICATION_METHOD2_
 - iketypes/IKEEXT_AUTHENTICATION_METHOD2_
 - IKEEXT_AUTHENTICATION_METHOD2
 - iketypes/IKEEXT_AUTHENTICATION_METHOD2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_AUTHENTICATION_METHOD2
---

# IKEEXT_AUTHENTICATION_METHOD2 structure


## -description

The <b>IKEEXT_AUTHENTICATION_METHOD2</b> structure specifies various parameters for IKE/Authip authentication.
[IKEEXT_AUTHENTICATION_METHOD0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method0)  is available.</div><div> </div>

## -struct-fields

### -field authenticationMethodType

Type: <b><a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a></b>

Type of authentication method.

### -field presharedKeyAuthentication

Type: <b><a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a></b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

### -field certificateAuthentication

Type: <b><a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2">IKEEXT_CERTIFICATE_AUTHENTICATION2</a></b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_CERTIFICATE</b>, <b>IKEEXT_CERTIFICATE_ECDSA_P256</b>, or <b>IKEEXT_CERTIFICATE_ECDSA_P384</b>.

### -field kerberosAuthentication

Type: [IKEEXT_KERBEROS_AUTHENTICATION1](./ns-iketypes-ikeext_certificate_authentication1.md)</b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_KERBEROS</b>.

### -field reservedAuthentication

Type: [IKEEXT_RESERVED_AUTHENTICATION0](./ns-iketypes-ikeext_eap_authentication0.md)</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_RESERVED</b>.

### -field ntlmV2Authentication

Type: [IKEEXT_NTLM_V2_AUTHENTICATION0](./ns-iketypes-ikeext_eap_authentication0.md)</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_NTLM_V2</b>.

### -field sslAuthentication

Type: <b><a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2">IKEEXT_CERTIFICATE_AUTHENTICATION2</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_SSL</b>, <b>IKEEXT_SSL_ECDSA_P256</b>, or <b>IKEEXT_SSL_ECDSA_P384</b>.

### -field cgaAuthentication

Type: [IKEEXT_IPV6_CGA_AUTHENTICATION0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_IPV6_CGA</b>.

### -field eapAuthentication

Type: [IKEEXT_EAP_AUTHENTICATION0](./ns-iketypes-ikeext_eap_authentication0.md)</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_EAP</b>.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
