---
UID: NS:ras._RASIKEV2_PROJECTION_INFO
title: RASIKEV2_PROJECTION_INFO (ras.h)
description: Contains projection information obtained during Internet Key Exchange (IKE) negotiation.
helpviewer_keywords: ["*PRASIKEV2_PROJECTION_INFO","IPSEC_CIPHER_TYPE_3DES","IPSEC_CIPHER_TYPE_AES_128","IPSEC_CIPHER_TYPE_AES_192","IPSEC_CIPHER_TYPE_AES_256","PRASIKEV2_PROJECTION_INFO","PRASIKEV2_PROJECTION_INFO structure pointer [RAS]","RASIKEV2_PROJECTION_INFO","RASIKEV2_PROJECTION_INFO structure [RAS]","RASIKEv2_AUTH_EAP","RASIKEv2_AUTH_MACHINECERTIFICATES","RASIKEv2_FLAGS_BEHIND_NAT","RASIKEv2_FLAGS_MOBIKESUPPORTED","RASIKEv2_FLAGS_SERVERBEHIND_NAT","ras/PRASIKEV2_PROJECTION_INFO","ras/RASIKEV2_PROJECTION_INFO","rras.rasikev2_projection_info"]
old-location: rras\rasikev2_projection_info.htm
tech.root: RRAS
ms.assetid: c88346f0-118e-4468-83b1-2dfc263e22f7
ms.date: 12/05/2018
ms.keywords: '*PRASIKEV2_PROJECTION_INFO, IPSEC_CIPHER_TYPE_3DES, IPSEC_CIPHER_TYPE_AES_128, IPSEC_CIPHER_TYPE_AES_192, IPSEC_CIPHER_TYPE_AES_256, PRASIKEV2_PROJECTION_INFO, PRASIKEV2_PROJECTION_INFO structure pointer [RAS], RASIKEV2_PROJECTION_INFO, RASIKEV2_PROJECTION_INFO structure [RAS], RASIKEv2_AUTH_EAP, RASIKEv2_AUTH_MACHINECERTIFICATES, RASIKEv2_FLAGS_BEHIND_NAT, RASIKEv2_FLAGS_MOBIKESUPPORTED, RASIKEv2_FLAGS_SERVERBEHIND_NAT, ras/PRASIKEV2_PROJECTION_INFO, ras/RASIKEV2_PROJECTION_INFO, rras.rasikev2_projection_info'
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: RASIKEV2_PROJECTION_INFO, *PRASIKEV2_PROJECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RASIKEV2_PROJECTION_INFO
 - ras/_RASIKEV2_PROJECTION_INFO
 - PRASIKEV2_PROJECTION_INFO
 - ras/PRASIKEV2_PROJECTION_INFO
 - RASIKEV2_PROJECTION_INFO
 - ras/RASIKEV2_PROJECTION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RASIKEV2_PROJECTION_INFO
---

# RASIKEV2_PROJECTION_INFO structure


## -description

The 
<b>RASIKEV2_PROJECTION_INFO</b> structure contains projection information obtained during Internet Key Exchange (IKE) negotiation.

## -struct-fields

### -field dwIPv4NegotiationError

A value that specifies the result of IPv4 negotiation. A value of zero indicates an IPv4 address has been assigned successfully. A nonzero value indicates failure, and is the fatal error that occurred during negotiation.

### -field ipv4Address

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV4ADDR</a>  structure  that contains a null-terminated Unicode string that specifies the IPv4 address of the local client. This string has the form "a.b.c.d". <b>ipv4Address</b> is valid only if <b>dwIPv4NegotiationError</b> is zero.

### -field ipv4ServerAddress

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV4ADDR</a> structure  that contains a null-terminated Unicode string that specifies the IPv4 address of the remote server. This string has the form "a.b.c.d". <b>ipv4ServerAddress</b> is valid only if <b>dwIPv4NegotiationError</b> is zero. If the address is not available, this member is an empty string.

### -field dwIPv6NegotiationError

A value that specifies the result of IPv6 negotiation. A value of zero indicates an IPv6 address has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during negotiation.

### -field ipv6Address

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV6ADDR</a>  structure  that contains a null-terminated Unicode string that specifies the IPv6 address of the local client. <b>ipv6Address</b> is valid only if <b>dwIPv6NegotiationError</b> is zero.

### -field ipv6ServerAddress

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV6ADDR</a> structure  that contains a null-terminated Unicode string that specifies the IPv6 address of the remote server. <b>ipv6ServerAddress</b> is valid only if <b>dwIPv6NegotiationError</b> is zero. If the address is not available, this member is an empty string.

### -field dwPrefixLength

A value that specifies the length, in bits, of the IPv6 address prefix.

### -field dwAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the remote server. The following authentication protocols are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASIKEv2_AUTH_MACHINECERTIFICATES"></a><a id="rasikev2_auth_machinecertificates"></a><a id="RASIKEV2_AUTH_MACHINECERTIFICATES"></a><dl>
<dt><b>RASIKEv2_AUTH_MACHINECERTIFICATES</b></dt>
</dl>
</td>
<td width="60%">
X.509 Public Key Infrastructure
                      Certificate (<a href="https://www.ietf.org/rfc/rfc2459.txt">RFC 2459</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASIKEv2_AUTH_EAP"></a><a id="rasikev2_auth_eap"></a><a id="RASIKEV2_AUTH_EAP"></a><dl>
<dt><b>RASIKEv2_AUTH_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol.

</td>
</tr>
</table>

### -field dwEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the local client. The value of this member is valid only if <b>dwAuthenticationProtocol</b> is <b>RASIKEv2_AUTH_EAP</b>.

### -field dwFlags

A bitmap of flags that can be any combination of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASIKEv2_FLAGS_MOBIKESUPPORTED"></a><a id="rasikev2_flags_mobikesupported"></a><a id="RASIKEV2_FLAGS_MOBIKESUPPORTED"></a><dl>
<dt><b>RASIKEv2_FLAGS_MOBIKESUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The client supports Mobile IKE (MOBIKE).

</td>
</tr>
<tr>
<td width="40%"><a id="RASIKEv2_FLAGS_BEHIND_NAT"></a><a id="rasikev2_flags_behind_nat"></a><a id="RASIKEV2_FLAGS_BEHIND_NAT"></a><dl>
<dt><b>RASIKEv2_FLAGS_BEHIND_NAT</b></dt>
</dl>
</td>
<td width="60%">
The client is behind Network Address Translation (NAT).

</td>
</tr>
<tr>
<td width="40%"><a id="RASIKEv2_FLAGS_SERVERBEHIND_NAT"></a><a id="rasikev2_flags_serverbehind_nat"></a><a id="RASIKEV2_FLAGS_SERVERBEHIND_NAT"></a><dl>
<dt><b>RASIKEv2_FLAGS_SERVERBEHIND_NAT</b></dt>
</dl>
</td>
<td width="60%">
The server is behind Network Address Translation (NAT).

</td>
</tr>
</table>

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
3DES encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_128"></a><a id="ipsec_cipher_type_aes_128"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_128</b></dt>
</dl>
</td>
<td width="60%">
AES-128 encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_192"></a><a id="ipsec_cipher_type_aes_192"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_192</b></dt>
</dl>
</td>
<td width="60%">
AES-192 encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_CIPHER_TYPE_AES_256"></a><a id="ipsec_cipher_type_aes_256"></a><dl>
<dt><b>IPSEC_CIPHER_TYPE_AES_256</b></dt>
</dl>
</td>
<td width="60%">
AES-256 encryption.

</td>
</tr>
</table>

### -field numIPv4ServerAddresses

The number of available IPv4 addresses the server can switch to on the IKEv2 connection.

### -field ipv4ServerAddresses

A pointer to a <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV4ADDR</a> structure that contains the available IPv4 addresses the server can switch to on the IKEv2 connection.

### -field numIPv6ServerAddresses

The number of available IPv6 addresses the server can switch to on the IKEv2 connection.

### -field ipv6ServerAddresses

A pointer to a <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV6ADDR</a> structure that contains the available IPv6 addresses the server can switch to on the IKEv2 connection.

## -see-also

<a href="/windows/desktop/api/ras/ne-ras-rasprojection_info_type">RASPROJECTION_INFO_TYPE</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-structures">Remote Access Service Structures</a>