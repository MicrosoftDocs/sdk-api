---
UID: NS:mprapi._PPP_PROJECTION_INFO
title: PPP_PROJECTION_INFO (mprapi.h)
description: Contains information obtained during Point-to-Point (PPP) negotiation for Secure Socket Tunneling Protocol (SSTP), Point-to-Point Tunneling Protocol (PPTP), and Layer 2 Tunneling Protocol (L2TP). (PPP_PROJECTION_INFO)
helpviewer_keywords: ["*PPPP_PROJECTION_INFO","ERROR_PPP_NOT_CONVERGING","PPP_CCP_COMPRESSION","PPP_CCP_ENCRYPTION128BIT","PPP_CCP_ENCRYPTION40BIT","PPP_CCP_ENCRYPTION40BITOLD","PPP_CCP_ENCRYPTION56BIT","PPP_CCP_HISTORYLESS","PPP_IPCP_VJ","PPP_LCP_3_DES","PPP_LCP_ACFC","PPP_LCP_AES_128","PPP_LCP_AES_256","PPP_LCP_CHAP","PPP_LCP_CHAP_MD5","PPP_LCP_CHAP_MS","PPP_LCP_CHAP_MSV2","PPP_LCP_DES_56","PPP_LCP_EAP","PPP_LCP_MULTILINK_FRAMING","PPP_LCP_PAP","PPP_LCP_PFC","PPP_LCP_SSHF","PPP_PROJECTION_INFO","PPP_PROJECTION_INFO structure [RAS]","RASCCPCA_MPPC","RASCCPCA_STAC","mprapi/PPP_PROJECTION_INFO","rras.ppp_projection_info"]
old-location: rras\ppp_projection_info.htm
tech.root: RRAS
ms.assetid: f100a7d0-9f22-4cc6-8db0-684cff565e76
ms.date: 12/05/2018
ms.keywords: '*PPPP_PROJECTION_INFO, ERROR_PPP_NOT_CONVERGING, PPP_CCP_COMPRESSION, PPP_CCP_ENCRYPTION128BIT, PPP_CCP_ENCRYPTION40BIT, PPP_CCP_ENCRYPTION40BITOLD, PPP_CCP_ENCRYPTION56BIT, PPP_CCP_HISTORYLESS, PPP_IPCP_VJ, PPP_LCP_3_DES, PPP_LCP_ACFC, PPP_LCP_AES_128, PPP_LCP_AES_256, PPP_LCP_CHAP, PPP_LCP_CHAP_MD5, PPP_LCP_CHAP_MS, PPP_LCP_CHAP_MSV2, PPP_LCP_DES_56, PPP_LCP_EAP, PPP_LCP_MULTILINK_FRAMING, PPP_LCP_PAP, PPP_LCP_PFC, PPP_LCP_SSHF, PPP_PROJECTION_INFO, PPP_PROJECTION_INFO structure [RAS], RASCCPCA_MPPC, RASCCPCA_STAC, mprapi/PPP_PROJECTION_INFO, rras.ppp_projection_info'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: PPP_PROJECTION_INFO, *PPPP_PROJECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_PROJECTION_INFO
 - mprapi/_PPP_PROJECTION_INFO
 - PPPP_PROJECTION_INFO
 - mprapi/PPPP_PROJECTION_INFO
 - PPP_PROJECTION_INFO
 - mprapi/PPP_PROJECTION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_PROJECTION_INFO
---

# PPP_PROJECTION_INFO structure


## -description

The 
<b>PPP_PROJECTION_INFO</b> structure contains information obtained during Point-to-Point (PPP) negotiation for Secure Socket Tunneling Protocol (SSTP), Point-to-Point Tunneling Protocol (PPTP), and Layer 2 Tunneling Protocol (L2TP).

## -struct-fields

### -field dwIPv4NegotiationError

A value that specifies the result of PPP IPv4  Network control protocol negotiation. A value of zero indicates Ipv4 has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field wszAddress

An array that contains a Unicode string that specifies the IPv4 address of the local client. This string has the form "a.b.c.d". <b>wszAddress</b> is valid only if <b>dwIPv4NegotiationError</b> is zero.

### -field wszRemoteAddress

An array that contains a Unicode string that specifies the IPv4 address of the remote server. This string has the form "a.b.c.d". <b>wszRemoteAddress</b> is valid only if <b>dwIPv4NegotiationError</b> is zero. If the address is not available, this member is an empty string.

### -field dwIPv4Options

A value that specifies IPCP options for the local client.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_IPCP_VJ"></a><a id="ppp_ipcp_vj"></a><dl>
<dt><b>PPP_IPCP_VJ</b></dt>
</dl>
</td>
<td width="60%">
Indicates that IP datagrams sent by the local client are compressed using Van Jacobson compression.

</td>
</tr>
</table>

### -field dwIPv4RemoteOptions

A value that specifies IPCP options for the remote server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_IPCP_VJ"></a><a id="ppp_ipcp_vj"></a><dl>
<dt><b>PPP_IPCP_VJ</b></dt>
</dl>
</td>
<td width="60%">
Indicates that IP datagrams sent by the remote server (that is, received by the local computer) are compressed using Van Jacobson compression.

</td>
</tr>
</table>

### -field IPv4SubInterfaceIndex

A value that specifies the IPv4 subinterface   index corresponding to the connection on the server.

### -field dwIPv6NegotiationError

A value that specifies the result of PPP IPv6  Network control protocol negotiation. A value of zero indicates Ipv6 has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field bInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the client. The last 64 bits of a 128-bit IPv6 internet address are considered the "interface identifier," which provides a strong level of uniqueness for the preceding 64-bits. <b>bInterfaceIdentifier</b> is valid only if <b>dwIPv6NegotiationError</b> is zero and must not be zero.

### -field bRemoteInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the server. The last 64 bits of a 128-bit IPv6 internet address are considered the "interface identifier," which provides a strong level of uniqueness for the preceding 64-bits. <b>bInterfaceIdentifier</b> is valid only if <b>dwIPv6NegotiationError</b> is zero and must not be zero.

### -field bPrefix

A value that specifies the client interface IPv6  address prefix.

### -field dwPrefixLength

A value that specifies the length, in bits, of <b>bPrefix</b>.

### -field IPv6SubInterfaceIndex

A value that specifies the IPv6 subinterface   index corresponding to the connection on the server.

### -field dwLcpError

A value that specifies the result of PPP LCP negotiation. A value of zero indicates LCP has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field dwAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the local client. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_PAP"></a><a id="ppp_lcp_pap"></a><dl>
<dt><b>PPP_LCP_PAP</b></dt>
</dl>
</td>
<td width="60%">
Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP"></a><a id="ppp_lcp_chap"></a><dl>
<dt><b>PPP_LCP_CHAP</b></dt>
</dl>
</td>
<td width="60%">
Challenge Handshake Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_EAP"></a><a id="ppp_lcp_eap"></a><dl>
<dt><b>PPP_LCP_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol.

</td>
</tr>
</table>

### -field dwAuthenticationData

A value that specifies additional information about the authentication protocol specified by <b>dwAuthenticationProtocol</b>. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MD5"></a><a id="ppp_lcp_chap_md5"></a><dl>
<dt><b>PPP_LCP_CHAP_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 CHAP

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MS"></a><a id="ppp_lcp_chap_ms"></a><dl>
<dt><b>PPP_LCP_CHAP_MS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MSV2"></a><a id="ppp_lcp_chap_msv2"></a><dl>
<dt><b>PPP_LCP_CHAP_MSV2</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP version 2.

</td>
</tr>
</table>

### -field dwRemoteAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the remote server. <b>dwAuthenticationProtocol</b> and <b>dwRemoteAuthenticationProtocol</b> will differ when demand dial uses different authentication protocols on the client and server. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_PAP"></a><a id="ppp_lcp_pap"></a><dl>
<dt><b>PPP_LCP_PAP</b></dt>
</dl>
</td>
<td width="60%">
Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP"></a><a id="ppp_lcp_chap"></a><dl>
<dt><b>PPP_LCP_CHAP</b></dt>
</dl>
</td>
<td width="60%">
Challenge Handshake Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_EAP"></a><a id="ppp_lcp_eap"></a><dl>
<dt><b>PPP_LCP_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol.

</td>
</tr>
</table>

### -field dwRemoteAuthenticationData

A value that specifies additional information about the authentication protocol specified by <b>dwRemoteAuthenticationProtocol</b>.  <b>dwAuthenticationData</b> and <b>dwRemoteAuthenticationData</b> will differ when demand dial uses different authentication protocols on the client and server. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MD5"></a><a id="ppp_lcp_chap_md5"></a><dl>
<dt><b>PPP_LCP_CHAP_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MS"></a><a id="ppp_lcp_chap_ms"></a><dl>
<dt><b>PPP_LCP_CHAP_MS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MSV2"></a><a id="ppp_lcp_chap_msv2"></a><dl>
<dt><b>PPP_LCP_CHAP_MSV2</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP version 2.

</td>
</tr>
</table>

### -field dwLcpTerminateReason

Reserved for future use. Must be zero.

### -field dwLcpRemoteTerminateReason

Reserved for future use. Must be zero.

### -field dwLcpOptions

A value that specifies information about LCP options in use by the local client. This member is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_MULTILINK_FRAMING"></a><a id="ppp_lcp_multilink_framing"></a><dl>
<dt><b>PPP_LCP_MULTILINK_FRAMING</b></dt>
</dl>
</td>
<td width="60%">
The connection is using multilink.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_PFC"></a><a id="ppp_lcp_pfc"></a><dl>
<dt><b>PPP_LCP_PFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Protocol Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_ACFC_"></a><a id="ppp_lcp_acfc_"></a><dl>
<dt><b>PPP_LCP_ACFC </b></dt>
</dl>
</td>
<td width="60%">
The connection is using Address and Control Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_SSHF"></a><a id="ppp_lcp_sshf"></a><dl>
<dt><b>PPP_LCP_SSHF</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Short Sequence Number Header Format (see RFC 1990).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_DES_56"></a><a id="ppp_lcp_des_56"></a><dl>
<dt><b>PPP_LCP_DES_56</b></dt>
</dl>
</td>
<td width="60%">
The connection is using DES 56-bit encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_3_DES"></a><a id="ppp_lcp_3_des"></a><dl>
<dt><b>PPP_LCP_3_DES</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Triple DES Encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_AES_128"></a><a id="ppp_lcp_aes_128"></a><dl>
<dt><b>PPP_LCP_AES_128</b></dt>
</dl>
</td>
<td width="60%">
The connection is using 128-bit AES Encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_AES_256"></a><a id="ppp_lcp_aes_256"></a><dl>
<dt><b>PPP_LCP_AES_256</b></dt>
</dl>
</td>
<td width="60%">
The connection is using 256-bit AES Encryption. 

</td>
</tr>
</table>

### -field dwLcpRemoteOptions

A value that specifies information about LCP options in use by the remote server. This member is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_MULTILINK_FRAMING"></a><a id="ppp_lcp_multilink_framing"></a><dl>
<dt><b>PPP_LCP_MULTILINK_FRAMING</b></dt>
</dl>
</td>
<td width="60%">
The connection is using multilink.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_PFC"></a><a id="ppp_lcp_pfc"></a><dl>
<dt><b>PPP_LCP_PFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Protocol Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_ACFC_"></a><a id="ppp_lcp_acfc_"></a><dl>
<dt><b>PPP_LCP_ACFC </b></dt>
</dl>
</td>
<td width="60%">
The connection is using Address and Control Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_SSHF"></a><a id="ppp_lcp_sshf"></a><dl>
<dt><b>PPP_LCP_SSHF</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Short Sequence Number Header Format (see RFC 1990).

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_DES_56"></a><a id="ppp_lcp_des_56"></a><dl>
<dt><b>PPP_LCP_DES_56</b></dt>
</dl>
</td>
<td width="60%">
The connection is using DES 56-bit encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_3_DES"></a><a id="ppp_lcp_3_des"></a><dl>
<dt><b>PPP_LCP_3_DES</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Triple DES Encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_AES_128"></a><a id="ppp_lcp_aes_128"></a><dl>
<dt><b>PPP_LCP_AES_128</b></dt>
</dl>
</td>
<td width="60%">
The connection is using 128-bit AES Encryption

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_AES_256"></a><a id="ppp_lcp_aes_256"></a><dl>
<dt><b>PPP_LCP_AES_256</b></dt>
</dl>
</td>
<td width="60%">
The connection is using 256-bit AES Encryption. 

</td>
</tr>
</table>

### -field dwEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the local client. The value of this member is valid only if <b>dwAuthenticationProtocol</b> is <b>PPP_LCP_EAP</b>.

### -field dwRemoteEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the remote server. The value of this member is valid only if <b>dwRemoteAuthenticationProtocol</b> is <b>PPP_LCP_EAP</b>.

### -field dwCcpError

A value that specifies the result of PPP CCP negotiation. A value of zero indicates CCP has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field dwCompressionAlgorithm

A value that specifies the compression algorithm used by the local client. The following table shows the possible values for this member.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_MPPC"></a><a id="rasccpca_mppc"></a><dl>
<dt><b>RASCCPCA_MPPC</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Compression (MPPC) Protocol (<a href="https://www.ietf.org/rfc/rfc2118.txt">RFC 2118</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_STAC"></a><a id="rasccpca_stac"></a><dl>
<dt><b>RASCCPCA_STAC</b></dt>
</dl>
</td>
<td width="60%">
STAC option 4 (<a href="https://www.ietf.org/rfc/rfc1974.txt">RFC 1974</a>).

</td>
</tr>
</table>

### -field dwCcpOptions

A value that specifies the compression types available on the local client. The following types are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_COMPRESSION"></a><a id="ppp_ccp_compression"></a><dl>
<dt><b>PPP_CCP_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_HISTORYLESS"></a><a id="ppp_ccp_historyless"></a><dl>
<dt><b>PPP_CCP_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BITOLD"></a><a id="ppp_ccp_encryption40bitold"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BIT"></a><a id="ppp_ccp_encryption40bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION56BIT"></a><a id="ppp_ccp_encryption56bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION128BIT"></a><a id="ppp_ccp_encryption128bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 128-bit keys.

</td>
</tr>
</table>
 

The last three options are used when a connection is made over Layer 2 Tunneling Protocol (L2TP), and the connection uses IPSec encryption.

### -field dwRemoteCompressionAlgorithm

A value that specifies the compression algorithm used by the remote server. The following algorithms are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_MPPC"></a><a id="rasccpca_mppc"></a><dl>
<dt><b>RASCCPCA_MPPC</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Compression (MPPC) Protocol (
<a href="https://www.ietf.org/rfc/rfc2118.txt">RFC 2118</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_STAC"></a><a id="rasccpca_stac"></a><dl>
<dt><b>RASCCPCA_STAC</b></dt>
</dl>
</td>
<td width="60%">
STAC option 4 (
<a href="https://www.ietf.org/rfc/rfc1974.txt">RFC 1974</a>).

</td>
</tr>
</table>

### -field dwCcpRemoteOptions

A value that specifies the compression types available on the remote server. The following types are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_COMPRESSION"></a><a id="ppp_ccp_compression"></a><dl>
<dt><b>PPP_CCP_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_HISTORYLESS"></a><a id="ppp_ccp_historyless"></a><dl>
<dt><b>PPP_CCP_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BITOLD"></a><a id="ppp_ccp_encryption40bitold"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BIT"></a><a id="ppp_ccp_encryption40bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION56BIT"></a><a id="ppp_ccp_encryption56bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION128BIT"></a><a id="ppp_ccp_encryption128bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 128-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_PPP_NOT_CONVERGING"></a><a id="error_ppp_not_converging"></a><dl>
<dt><b>ERROR_PPP_NOT_CONVERGING</b></dt>
</dl>
</td>
<td width="60%">
The remote computer and RRAS could not converge on address negotiation.

</td>
</tr>
</table>
 

The last three options are used when a connection is made over Layer 2 Tunneling Protocol (L2TP), and the connection uses IPSec encryption.

## -see-also

<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>
