---
UID: NS:ras._RASPPP_PROJECTION_INFO
title: RASPPP_PROJECTION_INFO (ras.h)
description: Contains information obtained during Point-to-Point (PPP) negotiation of Internet Protocol version 4 (IPv4) and IPv6 projection operations, and PPP Link Control Protocol (LCP)/multilink, and Compression Control Protocol (CCP) negotiation.
helpviewer_keywords: ["*PRASPPP_PROJECTION_INFO","RASCCPCA_MPPC","RASCCPCA_STAC","RASCCPO_COMPRESSION","RASCCPO_ENCRYPTION128BIT","RASCCPO_ENCRYPTION40BIT","RASCCPO_ENCRYPTION40BITOLD","RASCCPO_ENCRYPTION56BIT","RASCCPO_HISTORYLESS","RASIPO_VJ","RASLCPAD_CHAP_MD5","RASLCPAD_CHAP_MS","RASLCPAD_CHAP_MSV2","RASLCPAP_CHAP","RASLCPAP_EAP","RASLCPAP_PAP","RASLCPAP_SPAP","RASLCPO_3_DES","RASLCPO_ACFC","RASLCPO_DES_56","RASLCPO_PFC","RASLCPO_SSHF","RASPPP_PROJECTION_INFO","RASPPP_PROJECTION_INFO structure [RAS]","ras/RASPPP_PROJECTION_INFO","rras.rasppp_projection_info"]
old-location: rras\rasppp_projection_info.htm
tech.root: RRAS
ms.assetid: 8394b843-75f0-4bbd-9ad8-6f4b5dc4bf7b
ms.date: 12/05/2018
ms.keywords: '*PRASPPP_PROJECTION_INFO, RASCCPCA_MPPC, RASCCPCA_STAC, RASCCPO_COMPRESSION, RASCCPO_ENCRYPTION128BIT, RASCCPO_ENCRYPTION40BIT, RASCCPO_ENCRYPTION40BITOLD, RASCCPO_ENCRYPTION56BIT, RASCCPO_HISTORYLESS, RASIPO_VJ, RASLCPAD_CHAP_MD5, RASLCPAD_CHAP_MS, RASLCPAD_CHAP_MSV2, RASLCPAP_CHAP, RASLCPAP_EAP, RASLCPAP_PAP, RASLCPAP_SPAP, RASLCPO_3_DES, RASLCPO_ACFC, RASLCPO_DES_56, RASLCPO_PFC, RASLCPO_SSHF, RASPPP_PROJECTION_INFO, RASPPP_PROJECTION_INFO structure [RAS], ras/RASPPP_PROJECTION_INFO, rras.rasppp_projection_info'
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
req.typenames: RASPPP_PROJECTION_INFO, *PRASPPP_PROJECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RASPPP_PROJECTION_INFO
 - ras/_RASPPP_PROJECTION_INFO
 - PRASPPP_PROJECTION_INFO
 - ras/PRASPPP_PROJECTION_INFO
 - RASPPP_PROJECTION_INFO
 - ras/RASPPP_PROJECTION_INFO
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
 - RASPPP_PROJECTION_INFO
---

# RASPPP_PROJECTION_INFO structure


## -description

The 
<b>RASPPP_PROJECTION_INFO</b> structure contains information obtained during Point-to-Point (PPP) negotiation of Internet Protocol version 4 (IPv4) and IPv6 projection operations, and PPP Link Control Protocol (LCP)/multilink, and Compression Control Protocol (CCP) negotiation.

## -struct-fields

### -field dwIPv4NegotiationError

A value that specifies the result of PPP IPv4  network control protocol negotiation. A value of zero indicates Ipv4 has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field ipv4Address

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV4ADDR</a> that contains a null-terminated Unicode string that specifies the IPv4 address of the local client. This string has the form "a.b.c.d". <b>ipv4Address</b> is valid only if <b>dwIPv4NegotiationError</b> is zero.

### -field ipv4ServerAddress

A <a href="/windows/desktop/RRAS/remote-access-service-data-types">RASIPV4ADDR</a> structure that contains a Unicode string that specifies the IPv4 address of the remote server. This string has the form "a.b.c.d". <b>ipv4ServerAddress</b> is valid only if <b>dwIPv4NegotiationError</b> is zero. If the address is not available, this member is an empty string.

### -field dwIPv4Options

A value that specifies Internet Protocol Control Protocol (IPCP) options for the local client.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASIPO_VJ"></a><a id="rasipo_vj"></a><dl>
<dt><b>RASIPO_VJ</b></dt>
</dl>
</td>
<td width="60%">
Indicates that IP datagrams sent by the local client are compressed using Van Jacobson compression.

</td>
</tr>
</table>

### -field dwIPv4ServerOptions

A value that specifies IPCP options for the remote server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASIPO_VJ"></a><a id="rasipo_vj"></a><dl>
<dt><b>RASIPO_VJ</b></dt>
</dl>
</td>
<td width="60%">
Indicates that IP datagrams sent by the remote server (that is, received by the local computer) are compressed using Van Jacobson compression.

</td>
</tr>
</table>

### -field dwIPv6NegotiationError

A value that specifies the result of PPP IPv6  network control protocol negotiation. A value of zero indicates Ipv6 has been negotiated successfully. A nonzero value indicates failure, and is the fatal error that occurred during the control protocol negotiation.

### -field bInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the client. The last 64 bits of a 128-bit IPv6 internet address are considered the "interface identifier," which provides a strong level of uniqueness for the preceding 64-bits. <b>bInterfaceIdentifier</b> must not be zero and is valid only if <b>dwIPv6NegotiationError</b> is zero.

### -field bServerInterfaceIdentifier

An array that specifies the 64-bit IPv6 interface identifier of the server. The last 64 bits of a 128-bit IPv6 internet address are considered the "interface identifier," which provides a strong level of uniqueness for the preceding 64-bits. <b>bServerInterfaceIdentifier</b> must not be zero and is valid only if <b>dwIPv6NegotiationError</b> is zero.

### -field fBundled

A <b>BOOL</b> that is <b>TRUE</b> if the connection is composed of multiple links and <b>FALSE</b> otherwise.

### -field fMultilink

A <b>BOOL</b> that is <b>TRUE</b> if the connection supports multiple links and <b>FALSE</b> otherwise.

### -field dwAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the local client. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_PAP"></a><a id="raslcpap_pap"></a><dl>
<dt><b>RASLCPAP_PAP</b></dt>
</dl>
</td>
<td width="60%">
Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_SPAP"></a><a id="raslcpap_spap"></a><dl>
<dt><b>RASLCPAP_SPAP</b></dt>
</dl>
</td>
<td width="60%">
Shiva Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_CHAP"></a><a id="raslcpap_chap"></a><dl>
<dt><b>RASLCPAP_CHAP</b></dt>
</dl>
</td>
<td width="60%">
Challenge Handshake Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_EAP"></a><a id="raslcpap_eap"></a><dl>
<dt><b>RASLCPAP_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol.

</td>
</tr>
</table>

### -field dwAuthenticationData

A value that specifies additional information about the authentication protocol specified by <b>dwAuthenticationProtocol</b>. <b>dwAuthenticationData</b> and <b>dwServerAuthenticationData</b>  when different authentication protocols on the client and server. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MD5"></a><a id="raslcpad_chap_md5"></a><dl>
<dt><b>RASLCPAD_CHAP_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MS"></a><a id="raslcpad_chap_ms"></a><dl>
<dt><b>RASLCPAD_CHAP_MS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MSV2"></a><a id="raslcpad_chap_msv2"></a><dl>
<dt><b>RASLCPAD_CHAP_MSV2</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP version 2.

</td>
</tr>
</table>

### -field dwServerAuthenticationProtocol

A value that specifies the authentication protocol used to authenticate the remote server. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_PAP"></a><a id="raslcpap_pap"></a><dl>
<dt><b>RASLCPAP_PAP</b></dt>
</dl>
</td>
<td width="60%">
Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_SPAP"></a><a id="raslcpap_spap"></a><dl>
<dt><b>RASLCPAP_SPAP</b></dt>
</dl>
</td>
<td width="60%">
Shiva Password Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_CHAP"></a><a id="raslcpap_chap"></a><dl>
<dt><b>RASLCPAP_CHAP</b></dt>
</dl>
</td>
<td width="60%">
Challenge Handshake Authentication Protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAP_EAP"></a><a id="raslcpap_eap"></a><dl>
<dt><b>RASLCPAP_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol.

</td>
</tr>
</table>

### -field dwServerAuthenticationData

A value that specifies additional information about the authentication protocol specified by <b>dwServerAuthenticationProtocol</b>.  <b>dwAuthenticationData</b> and <b>dwServerAuthenticationData</b>  when different authentication protocols on the client and server. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MD5"></a><a id="raslcpad_chap_md5"></a><dl>
<dt><b>RASLCPAD_CHAP_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MS"></a><a id="raslcpad_chap_ms"></a><dl>
<dt><b>RASLCPAD_CHAP_MS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPAD_CHAP_MSV2"></a><a id="raslcpad_chap_msv2"></a><dl>
<dt><b>RASLCPAD_CHAP_MSV2</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP version 2.

</td>
</tr>
</table>

### -field dwEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the local client. The value of this member is valid only if <b>dwAuthenticationProtocol</b> is <b>RASLCPAPP_EAP.</b>.

### -field dwServerEapTypeId

A value that specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the remote server. The value of this member is valid only if <b>dwRemoteAuthenticationProtocol</b> is <b>RASLCPAPP_EAP.</b>.

### -field dwLcpOptions

A value that specifies information about LCP options in use by the local client. This member is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_PFC"></a><a id="raslcpo_pfc"></a><dl>
<dt><b>RASLCPO_PFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Protocol Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_ACFC"></a><a id="raslcpo_acfc"></a><dl>
<dt><b>RASLCPO_ACFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Address and Control Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_SSHF"></a><a id="raslcpo_sshf"></a><dl>
<dt><b>RASLCPO_SSHF</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Short Sequence Number Header Format (see RFC 1990).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_DES_56"></a><a id="raslcpo_des_56"></a><dl>
<dt><b>RASLCPO_DES_56</b></dt>
</dl>
</td>
<td width="60%">
The connection is using DES 56-bit encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_3_DES"></a><a id="raslcpo_3_des"></a><dl>
<dt><b>RASLCPO_3_DES</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Triple DES Encryption.

</td>
</tr>
</table>

### -field dwLcpServerOptions

A value that specifies information about LCP options in use by the remote server. This member is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_PFC"></a><a id="raslcpo_pfc"></a><dl>
<dt><b>RASLCPO_PFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Protocol Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_ACFC"></a><a id="raslcpo_acfc"></a><dl>
<dt><b>RASLCPO_ACFC</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Address and Control Field Compression (<a href="https://www.ietf.org/rfc/rfc1172.txt">RFC 1172</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_SSHF"></a><a id="raslcpo_sshf"></a><dl>
<dt><b>RASLCPO_SSHF</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Short Sequence Number Header Format (see RFC 1990).

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_DES_56"></a><a id="raslcpo_des_56"></a><dl>
<dt><b>RASLCPO_DES_56</b></dt>
</dl>
</td>
<td width="60%">
The connection is using DES 56-bit encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_3_DES"></a><a id="raslcpo_3_des"></a><dl>
<dt><b>RASLCPO_3_DES</b></dt>
</dl>
</td>
<td width="60%">
The connection is using Triple DES Encryption.

</td>
</tr>
</table>

### -field dwCcpError

### -field dwCcpCompressionAlgorithm

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

### -field dwCcpServerCompressionAlgorithm

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

### -field dwCcpOptions

A value that specifies the compression types available on the local client. The following types are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_COMPRESSION"></a><a id="rasccpo_compression"></a><dl>
<dt><b>RASCCPO_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_HISTORYLESS"></a><a id="rasccpo_historyless"></a><dl>
<dt><b>RASCCPO_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION40BITOLD"></a><a id="rasccpo_encryption40bitold"></a><dl>
<dt><b>RASCCPO_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION40BIT"></a><a id="rasccpo_encryption40bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION56BIT"></a><a id="rasccpo_encryption56bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION128BIT"></a><a id="rasccpo_encryption128bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 128-bit keys.

</td>
</tr>
</table>

### -field dwCcpServerOptions

A value that specifies the compression types available on the remote server. The following types are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_COMPRESSION"></a><a id="rasccpo_compression"></a><dl>
<dt><b>RASCCPO_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_HISTORYLESS"></a><a id="rasccpo_historyless"></a><dl>
<dt><b>RASCCPO_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION40BITOLD"></a><a id="rasccpo_encryption40bitold"></a><dl>
<dt><b>RASCCPO_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION40BIT"></a><a id="rasccpo_encryption40bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION56BIT"></a><a id="rasccpo_encryption56bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPO_ENCRYPTION128BIT"></a><a id="rasccpo_encryption128bit"></a><dl>
<dt><b>RASCCPO_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE compression using 128-bit keys.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rasgetprojectioninfoex">RasGetProjectionInfoEx</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-structures">Remote Access Service Structures</a>