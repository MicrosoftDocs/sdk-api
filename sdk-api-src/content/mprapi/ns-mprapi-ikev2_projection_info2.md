---
UID: NS:mprapi._IKEV2_PROJECTION_INFO2
title: IKEV2_PROJECTION_INFO2 (mprapi.h)
description: Contains information obtained during Internet Key Exchange (IKE) negotiation. (IKEV2_PROJECTION_INFO2)
helpviewer_keywords: ["*PIKEV2_PROJECTION_INFO2","IKEV2_PROJECTION_INFO2","IKEV2_PROJECTION_INFO2 structure [RAS]","IPSEC_CIPHER_TYPE_3DES","IPSEC_CIPHER_TYPE_AES_128","IPSEC_CIPHER_TYPE_AES_192","IPSEC_CIPHER_TYPE_AES_256","MPRAPI_IKEV2_AUTH_USING_CERT","MPRAPI_IKEV2_AUTH_USING_EAP","PIKEV2_PROJECTION_INFO2","PIKEV2_PROJECTION_INFO2 structure pointer [RAS]","mprapi/IKEV2_PROJECTION_INFO2","mprapi/PIKEV2_PROJECTION_INFO2","rras.ikev2_projection_info2"]
old-location: rras\ikev2_projection_info2.htm
tech.root: RRAS
ms.assetid: 577a276e-e2f4-46d6-ae0b-2ba0f0bac67f
ms.date: 12/05/2018
ms.keywords: '*PIKEV2_PROJECTION_INFO2, IKEV2_PROJECTION_INFO2, IKEV2_PROJECTION_INFO2 structure [RAS], IPSEC_CIPHER_TYPE_3DES, IPSEC_CIPHER_TYPE_AES_128, IPSEC_CIPHER_TYPE_AES_192, IPSEC_CIPHER_TYPE_AES_256, MPRAPI_IKEV2_AUTH_USING_CERT, MPRAPI_IKEV2_AUTH_USING_EAP, PIKEV2_PROJECTION_INFO2, PIKEV2_PROJECTION_INFO2 structure pointer [RAS], mprapi/IKEV2_PROJECTION_INFO2, mprapi/PIKEV2_PROJECTION_INFO2, rras.ikev2_projection_info2'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEV2_PROJECTION_INFO2, *PIKEV2_PROJECTION_INFO2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IKEV2_PROJECTION_INFO2
 - mprapi/_IKEV2_PROJECTION_INFO2
 - PIKEV2_PROJECTION_INFO2
 - mprapi/PIKEV2_PROJECTION_INFO2
 - IKEV2_PROJECTION_INFO2
 - mprapi/IKEV2_PROJECTION_INFO2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mprapi.h
api_name:
 - IKEV2_PROJECTION_INFO2
---

# IKEV2_PROJECTION_INFO2 structure


## -description

Contains information obtained during Internet Key Exchange (IKE) negotiation.

## -struct-fields

### -field dwIPv4NegotiationError

A value that specifies the result of IPv4 negotiation. A value of zero indicates an IPv4 address has been assigned successfully. A nonzero value indicates failure, and is the fatal error that occurred during negotiation.

### -field wszAddress

An null-terminated Unicode string that specifies the IPv4 address of the local client. The string has the form "a.b.c.d". The <b>wszAddress</b> member is valid only if the <b>dwIPv4NegotiationError</b> member is 0.

### -field wszRemoteAddress

A null-terminated Unicode string that specifies the IPv4 address of the remote server. This string has the form "a.b.c.d". The <b>wszRemoteAddress</b> member is valid only if the <b>dwIPv4NegotiationError</b> member is zero. If the address is not available, this member is an empty string.

### -field IPv4SubInterfaceIndex

A value that specifies the IPv4 subinterface index corresponding to the connection on the server.

### -field dwIPv6NegotiationError

A value that specifies the result of IPv6 negotiation. A value of 0 indicates an IPv6 address has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during negotiation.

### -field bInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the client. The last 64-bits of a 128-bit IPv6 internet address are considered the interface identifier, which provides a strong level of uniqueness for the preceding 64-bits. The <b>bInterfaceIdentifier</b> member is valid only if the <b>dwIPv6NegotiationError</b> member is 0. The <i>bInterfaceIdentifier</i> member must not be 0.

### -field bRemoteInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the server. The last 64 bits of a 128-bit IPv6 internet address are considered the interface identifier, which provides a strong level of uniqueness for the preceding 64 bits. The <b>bInterfaceIdentifier</b> member must not be 0 and is valid only if the <b>dwIPv6NegotiationError</b> member  is zero.

### -field bPrefix

A value that specifies the client interface IPv6 address prefix.

### -field dwPrefixLength

A value that specifies the length, in bits, of the <b>bPrefix</b> member.

### -field IPv6SubInterfaceIndex

A value that specifies the IPv6 subinterface index corresponding to the connection on the server.

### -field dwOptions

Not implemented.

### -field dwAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the remote server. The following authentication protocols are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_AUTH_USING_CERT"></a><a id="mprapi_ikev2_auth_using_cert"></a><dl>
<dt><b>MPRAPI_IKEV2_AUTH_USING_CERT</b></dt>
</dl>
</td>
<td width="60%">
X.509 Public Key Infrastructure Certificate (described in RFC 2459)

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_AUTH_USING_EAP"></a><a id="mprapi_ikev2_auth_using_eap"></a><dl>
<dt><b>MPRAPI_IKEV2_AUTH_USING_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol

</td>
</tr>
</table>

### -field dwEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the local client. The value of this member is valid only if the <b>dwAuthenticationProtocol</b> member is <b>MPRAPI_IKEV2_AUTH_USING_EAP</b>.

### -field dwEmbeddedEAPTypeId

A value that specifies the type identifier of the inner EAP method used in the EAP authentication. The value of this member is valid only if the <b>dwEapTypeId</b> member is set to <b>PEAP</b> defined in IANA-EAP.

### -field dwCompressionAlgorithm

Not implemented.

### -field dwEncryptionMethod

A value that specifies the encryption method used in the connection. The following encryption methods are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_3DES"></a><a id="ipsec_cipher_type_3des"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_3DES</b></dt>
</dl>
</td>
<td width="60%">
3DES encryption

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_128"></a><a id="ipsec_cipher_type_aes_128"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_128</b></dt>
</dl>
</td>
<td width="60%">
AES-128 encryption

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_192"></a><a id="ipsec_cipher_type_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_192</b></dt>
</dl>
</td>
<td width="60%">
AES-192 encryption

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_256"></a><a id="ipsec_cipher_type_aes_256"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_256</b></dt>
</dl>
</td>
<td width="60%">
AES-256 encryption

</td>
</tr>
</table>

