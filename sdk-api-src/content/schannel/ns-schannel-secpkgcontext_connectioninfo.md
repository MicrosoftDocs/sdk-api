---
UID: NS:schannel._SecPkgContext_ConnectionInfo
title: SecPkgContext_ConnectionInfo (schannel.h)
description: The SecPkgContext_ConnectionInfo structure contains protocol and cipher information. This structure is used by the InitializeSecurityContext (Schannel) function.This attribute is supported only by the Schannel security support provider (SSP).
helpviewer_keywords: ["*PSecPkgContext_ConnectionInfo","0 (Zero)","CALG_3DES","CALG_AES_128","CALG_AES_256","CALG_DES","CALG_DH_EPHEM","CALG_MD5","CALG_RC2","CALG_RC4","CALG_RSA_KEYX","CALG_SHA","PSecPkgContext_ConnectionInfo","PSecPkgContext_ConnectionInfo structure pointer [Security]","SP_PROT_PCT1_CLIENT","SP_PROT_PCT1_SERVER","SP_PROT_SSL2_CLIENT","SP_PROT_SSL2_SERVER","SP_PROT_SSL3_CLIENT","SP_PROT_SSL3_SERVER","SP_PROT_TLS1_1_CLIENT","SP_PROT_TLS1_1_SERVER","SP_PROT_TLS1_2_CLIENT","SP_PROT_TLS1_2_SERVER","SP_PROT_TLS1_CLIENT","SP_PROT_TLS1_SERVER","SecPkgContext_ConnectionInfo","SecPkgContext_ConnectionInfo structure [Security]","_ssp_secpkgcontext_connectioninfo","schannel/PSecPkgContext_ConnectionInfo","schannel/SecPkgContext_ConnectionInfo","security.secpkgcontext_connectioninfo"]
old-location: security\secpkgcontext_connectioninfo.htm
tech.root: security
ms.assetid: 5380c03b-d2c5-4a0d-96a1-c39305b9c9ac
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_ConnectionInfo, 0 (Zero), CALG_3DES, CALG_AES_128, CALG_AES_256, CALG_DES, CALG_DH_EPHEM, CALG_MD5, CALG_RC2, CALG_RC4, CALG_RSA_KEYX, CALG_SHA, PSecPkgContext_ConnectionInfo, PSecPkgContext_ConnectionInfo structure pointer [Security], SP_PROT_PCT1_CLIENT, SP_PROT_PCT1_SERVER, SP_PROT_SSL2_CLIENT, SP_PROT_SSL2_SERVER, SP_PROT_SSL3_CLIENT, SP_PROT_SSL3_SERVER, SP_PROT_TLS1_1_CLIENT, SP_PROT_TLS1_1_SERVER, SP_PROT_TLS1_2_CLIENT, SP_PROT_TLS1_2_SERVER, SP_PROT_TLS1_CLIENT, SP_PROT_TLS1_SERVER, SecPkgContext_ConnectionInfo, SecPkgContext_ConnectionInfo structure [Security], _ssp_secpkgcontext_connectioninfo, schannel/PSecPkgContext_ConnectionInfo, schannel/SecPkgContext_ConnectionInfo, security.secpkgcontext_connectioninfo'
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SecPkgContext_ConnectionInfo, *PSecPkgContext_ConnectionInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_ConnectionInfo
 - schannel/_SecPkgContext_ConnectionInfo
 - PSecPkgContext_ConnectionInfo
 - schannel/PSecPkgContext_ConnectionInfo
 - SecPkgContext_ConnectionInfo
 - schannel/SecPkgContext_ConnectionInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SecPkgContext_ConnectionInfo
---

# SecPkgContext_ConnectionInfo structure


## -description

The <b>SecPkgContext_ConnectionInfo</b> structure contains protocol and cipher information. This structure is used by the 
<a href="/windows/win32/secauthn/initializesecuritycontext--schannel">InitializeSecurityContext (Schannel)</a> function.

This attribute is supported only by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

## -struct-fields

### -field dwProtocol

Protocol used to establish this connection. The following table describes the constants valid for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_SSL2_CLIENT"></a><a id="sp_prot_ssl2_client"></a><dl>
<dt><b>SP_PROT_SSL2_CLIENT</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 2.0 client-side. Superseded by SP_PROT_TLS1_CLIENT.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_SSL2_SERVER"></a><a id="sp_prot_ssl2_server"></a><dl>
<dt><b>SP_PROT_SSL2_SERVER</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 2.0 server-side. Superseded by SP_PROT_TLS1_SERVER.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_SSL3_CLIENT"></a><a id="sp_prot_ssl3_client"></a><dl>
<dt><b>SP_PROT_SSL3_CLIENT</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 3.0 client-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_SSL3_SERVER"></a><a id="sp_prot_ssl3_server"></a><dl>
<dt><b>SP_PROT_SSL3_SERVER</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 3.0 server-side.
</td>
</tr>
 
<tr>
<td width="40%"><a id="SP_PROT_TLS1_0_CLIENT"></a><a id="sp_prot_tls1_0_client"></a><dl>
<dt><b>SP_PROT_TLS1_0_CLIENT</b></dt>
<dt>128 (0x80)</dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/t-gly">Transport Layer Security</a> 1.0 client-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_TLS1_0_SERVER"></a><a id="sp_prot_tls1_0_server"></a><dl>
<dt><b>SP_PROT_TLS1_0_SERVER</b></dt>
<dt>64 (0x40)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.0 server-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_TLS1_1_CLIENT"></a><a id="sp_prot_tls1_1_client"></a><dl>
<dt><b>SP_PROT_TLS1_1_CLIENT</b></dt>
<dt>512 (0x200)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.1 client-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_TLS1_1_SERVER"></a><a id="sp_prot_tls1_1_server"></a><dl>
<dt><b>SP_PROT_TLS1_1_SERVER</b></dt>
<dt>256 (0x100)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.1 server-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_TLS1_2_CLIENT"></a><a id="sp_prot_tls1_2_client"></a><dl>
<dt><b>SP_PROT_TLS1_2_CLIENT</b></dt>
<dt>2048 (0x800)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.2 client-side.
</td>
</tr>
 
<tr>
<td width="40%"><a id="SP_PROT_TLS1_2_SERVER"></a><a id="sp_prot_tls1_2_server"></a><dl>
<dt><b>SP_PROT_TLS1_2_SERVER</b></dt>
<dt>1024 (0x400)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.2 server-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_TLS1_3_CLIENT"></a><a id="sp_prot_tls1_3_client"></a><dl>
<dt><b>SP_PROT_TLS1_3_CLIENT</b></dt>
<dt>8192 (0x2000)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.3 client-side.
</td>
</tr>
 
<tr>
<td width="40%"><a id="SP_PROT_TLS1_3_SERVER"></a><a id="sp_prot_tls1_3_server"></a><dl>
<dt><b>SP_PROT_TLS1_3_SERVER</b></dt>
<dt>4096 (0x1000)</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.3 server-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_DTLS1_0_CLIENT"></a><a id="sp_prot_dtls1_0_client"></a><dl>
<dt><b>SP_PROT_DTLS1_0_CLIENT</b></dt>
<dt>131072 (0x00020000)</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.0 client-side.
</td>
</tr>
 
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_0_SERVER"></a><a id="sp_prot_dtls1_0_server"></a><dl>
<dt><b>SP_PROT_DTLS1_0_SERVER</b></dt>
<dt>65536 (0x00010000)</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.0 server-side.
</td>
</tr>

<tr>
<td width="40%"><a id="SP_PROT_DTLS1_2_CLIENT"></a><a id="sp_prot_dtls1_2_client"></a><dl>
<dt><b>SP_PROT_DTLS1_2_CLIENT</b></dt>
<dt>524288 (0x00080000)</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.2 client-side.
</td>
</tr>
 
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_2_SERVER"></a><a id="sp_prot_dtls1_2_server"></a><dl>
<dt><b>SP_PROT_DTLS1_2_SERVER</b></dt>
<dt>262144 (0x00040000)</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.2 server-side.
</td>
</tr>

</table>

### -field aiCipher

Algorithm identifier (<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>) for the bulk encryption cipher used by this connection. The following table describes the constants valid for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_3DES"></a><a id="calg_3des"></a><dl>
<dt><b>CALG_3DES</b></dt>
</dl>
</td>
<td width="60%">
3DES block encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_AES_128"></a><a id="calg_aes_128"></a><dl>
<dt><b>CALG_AES_128</b></dt>
</dl>
</td>
<td width="60%">
AES 128-bit encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_AES_256"></a><a id="calg_aes_256"></a><dl>
<dt><b>CALG_AES_256</b></dt>
</dl>
</td>
<td width="60%">
AES 256-bit encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_DES"></a><a id="calg_des"></a><dl>
<dt><b>CALG_DES</b></dt>
</dl>
</td>
<td width="60%">
DES encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_RC2"></a><a id="calg_rc2"></a><dl>
<dt><b>CALG_RC2</b></dt>
</dl>
</td>
<td width="60%">
RC2 block encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_RC4"></a><a id="calg_rc4"></a><dl>
<dt><b>CALG_RC4</b></dt>
</dl>
</td>
<td width="60%">
RC4 stream encryption algorithm

</td>
</tr>
<tr>
<td width="40%"><a id="0__Zero_"></a><a id="0__zero_"></a><a id="0__ZERO_"></a><dl>
<dt><b>0 (Zero)</b></dt>
</dl>
</td>
<td width="60%">
No encryption

</td>
</tr>
</table>

### -field dwCipherStrength

Strength of the bulk encryption cipher, in bits. Can be one of the following values: 0, 40, 56, 128, 168, or 256.

### -field aiHash

<b>ALG_ID</b> indicating the <a href="/windows/desktop/SecGloss/h-gly">hash</a> used for generating <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Codes</a> (MACs). The following table describes the constants valid for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_MD5"></a><a id="calg_md5"></a><dl>
<dt><b>CALG_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 hashing algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_SHA"></a><a id="calg_sha"></a><dl>
<dt><b>CALG_SHA</b></dt>
</dl>
</td>
<td width="60%">
SHA hashing algorithm.

</td>
</tr>
</table>

### -field dwHashStrength

Strength of the hash, in bits: 128 or 160.

### -field aiExch

<b>ALG_ID</b> indicating the <a href="/windows/desktop/SecGloss/k-gly">key exchange algorithm</a> used to generate the shared master secret. The following table describes the constants valid for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALG_TYPE_ANY"></a><a id="alg_type_any"></a><dl>
<dt><b>ALG_TYPE_ANY</b></dt>
</dl>
</td>
<td width="60%">
Any key exchange algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_RSA_KEYX"></a><a id="calg_rsa_keyx"></a><dl>
<dt><b>CALG_RSA_KEYX</b></dt>
</dl>
</td>
<td width="60%">
RSA key exchange.

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_DH_EPHEM"></a><a id="calg_dh_ephem"></a><dl>
<dt><b>CALG_DH_EPHEM</b></dt>
</dl>
</td>
<td width="60%">
Diffie-Hellman key exchange.

</td>
</tr>
</table>

### -field dwExchStrength

Key length, in bits. For RSA key exchange, this member will typically contain one of the following values: 512, 768, 1024, or 2048.  For Diffie-Hellman key exchange, this member will typically contain one of the following values: 224, 256, 384 or 512.
