---
UID: NS:schannel._SCHANNEL_CRED
title: SCHANNEL_CRED (schannel.h)
description: Contains the data for an Schannel credential. (SCHANNEL_CRED)
helpviewer_keywords: ["*PSCHANNEL_CRED","PSCHANNEL_CRED","PSCHANNEL_CRED structure pointer [Security]","SCHANNEL_CRED","SCHANNEL_CRED structure [Security]","SCH_CRED_AUTO_CRED_VALIDATION","SCH_CRED_CACHE_ONLY_URL_RETRIEVAL_ON_CREATE","SCH_CRED_FORMAT_CERT_HASH","SCH_CRED_FORMAT_CERT_HASH_STORE","SCH_CRED_IGNORE_NO_REVOCATION_CHECK","SCH_CRED_IGNORE_REVOCATION_OFFLINE","SCH_CRED_MANUAL_CRED_VALIDATION","SCH_CRED_NO_DEFAULT_CREDS","SCH_CRED_NO_SERVERNAME_CHECK","SCH_CRED_NO_SYSTEM_MAPPER","SCH_CRED_REVOCATION_CHECK_CHAIN","SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT","SCH_CRED_REVOCATION_CHECK_END_CERT","SCH_CRED_USE_DEFAULT_CREDS","SCH_DISABLE_RECONNECTS","SCH_SEND_AUX_RECORD","SCH_SEND_ROOT_CERT","SCH_USE_PRESHAREDKEY_ONLY","SCH_USE_STRONG_CRYPTO","SP_PROT_DTLS1_0_CLIENT","SP_PROT_DTLS1_0_SERVER","SP_PROT_DTLS1_2_CLIENT","SP_PROT_DTLS1_2_SERVER","SP_PROT_DTLS1_X_CLIENT","SP_PROT_DTLS1_X_SERVER","SP_PROT_DTLS_CLIENT","SP_PROT_DTLS_SERVER","SP_PROT_PCT1_CLIENT","SP_PROT_PCT1_SERVER","SP_PROT_SSL2_CLIENT","SP_PROT_SSL2_SERVER","SP_PROT_SSL3_CLIENT","SP_PROT_SSL3_SERVER","SP_PROT_TLS1_0_CLIENT","SP_PROT_TLS1_0_SERVER","SP_PROT_TLS1_1_CLIENT","SP_PROT_TLS1_1_SERVER","SP_PROT_TLS1_2_CLIENT","SP_PROT_TLS1_2_SERVER","SP_PROT_TLS1_CLIENT","SP_PROT_TLS1_SERVER","_ssp_schannel_cred","schannel/PSCHANNEL_CRED","schannel/SCHANNEL_CRED","security.schannel_cred"]
old-location: security\schannel_cred.htm
tech.root: security
ms.assetid: 8398e029-473e-488f-a861-c7ceae07e678
ms.date: 12/05/2018
ms.keywords: '*PSCHANNEL_CRED, PSCHANNEL_CRED, PSCHANNEL_CRED structure pointer [Security], SCHANNEL_CRED, SCHANNEL_CRED structure [Security], SCH_CRED_AUTO_CRED_VALIDATION, SCH_CRED_CACHE_ONLY_URL_RETRIEVAL_ON_CREATE, SCH_CRED_FORMAT_CERT_HASH, SCH_CRED_FORMAT_CERT_HASH_STORE, SCH_CRED_IGNORE_NO_REVOCATION_CHECK, SCH_CRED_IGNORE_REVOCATION_OFFLINE, SCH_CRED_MANUAL_CRED_VALIDATION, SCH_CRED_NO_DEFAULT_CREDS, SCH_CRED_NO_SERVERNAME_CHECK, SCH_CRED_NO_SYSTEM_MAPPER, SCH_CRED_REVOCATION_CHECK_CHAIN, SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, SCH_CRED_REVOCATION_CHECK_END_CERT, SCH_CRED_USE_DEFAULT_CREDS, SCH_DISABLE_RECONNECTS, SCH_SEND_AUX_RECORD, SCH_SEND_ROOT_CERT, SCH_USE_PRESHAREDKEY_ONLY, SCH_USE_STRONG_CRYPTO, SP_PROT_DTLS1_0_CLIENT, SP_PROT_DTLS1_0_SERVER, SP_PROT_DTLS1_2_CLIENT, SP_PROT_DTLS1_2_SERVER, SP_PROT_DTLS1_X_CLIENT, SP_PROT_DTLS1_X_SERVER, SP_PROT_DTLS_CLIENT, SP_PROT_DTLS_SERVER, SP_PROT_PCT1_CLIENT, SP_PROT_PCT1_SERVER, SP_PROT_SSL2_CLIENT, SP_PROT_SSL2_SERVER, SP_PROT_SSL3_CLIENT, SP_PROT_SSL3_SERVER, SP_PROT_TLS1_0_CLIENT, SP_PROT_TLS1_0_SERVER, SP_PROT_TLS1_1_CLIENT, SP_PROT_TLS1_1_SERVER, SP_PROT_TLS1_2_CLIENT, SP_PROT_TLS1_2_SERVER, SP_PROT_TLS1_CLIENT, SP_PROT_TLS1_SERVER, _ssp_schannel_cred, schannel/PSCHANNEL_CRED, schannel/SCHANNEL_CRED, security.schannel_cred'
req.header: schannel.h
req.include-header: Schnlsp.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SCHANNEL_CRED, *PSCHANNEL_CRED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_CRED
 - schannel/_SCHANNEL_CRED
 - PSCHANNEL_CRED
 - schannel/PSCHANNEL_CRED
 - SCHANNEL_CRED
 - schannel/SCHANNEL_CRED
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
 - SCHANNEL_CRED
---

## -description

> [!NOTE]
> The **SCHANNEL_CRED** structure is deprecated. You should use [SCH_CREDENTIALS](../schannel/ns-schannel-sch_credentials.md) instead.

The <b>SCHANNEL_CRED</b> structure contains the data for an Schannel credential.

## -struct-fields

### -field dwVersion

Set to SCHANNEL_CRED_VERSION.

### -field cCreds

The number of structures in the <b>paCred</b> array.

### -field paCred

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures. Each pointer specifies a certificate that contains a <a href="/windows/desktop/SecGloss/p-gly">private key</a> to be used in authenticating the application. Typically, this array contains one structure for each key exchange method supported by the application.

Client applications often pass in an empty list and either depend on Schannel to find an appropriate certificate or create a certificate later if needed.

### -field hRootStore

Optional. Valid for server applications only. Handle to a certificate store that contains self-signed <a href="/windows/desktop/SecGloss/r-gly">root certificates</a> for <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> (CAs) trusted by the application. This member is used only by server-side applications that require client authentication.

### -field cMappers

Reserved.

### -field aphMappers

Reserved.

### -field _HMAPPER

### -field cSupportedAlgs

Number of algorithms in the <b>palgSupportedAlgs</b> array.

### -field palgSupportedAlgs

Optional. A pointer to an array of 
<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> algorithm identifiers that represent the algorithms supported by connections made with credentials acquired using this structure. If <b>cSupportedAlgs</b> is zero or <b>palgSupportedAlgs</b> is <b>NULL</b>, Schannel uses the system defaults.

Currently, the algorithm identifiers <b>CALG_AES</b>,
<b>CALG_AES_128</b>, and
<b>CALG_AES_256</b> are not supported.

### -field grbitEnabledProtocols

Optional. A <b>DWORD</b> that contains a bit string that represents the protocols supported by connections made with credentials acquired by using this structure. If this member is zero, Schannel selects the protocol. For new development, applications should set <b>grbitEnabledProtocols</b> to zero and use the protocol versions enabled on the system by default.

This member is used only by the Microsoft Unified Security Protocol Provider <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

The global system registry settings take precedence over this value. For example, if SSL3 is disabled in the registry, it cannot be enabled using this member.

This member can contain any of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_PCT1_SERVER"></a><a id="sp_prot_pct1_server"></a><dl>
<dt><b>SP_PROT_PCT1_SERVER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Private Communications Technology 1.0 server side.

<div class="alert"><b>Note</b> Obsolete.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_PCT1_CLIENT"></a><a id="sp_prot_pct1_client"></a><dl>
<dt><b>SP_PROT_PCT1_CLIENT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Private Communications Technology 1.0 client side. 

<div class="alert"><b>Note</b> Obsolete.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_SSL2_SERVER"></a><a id="sp_prot_ssl2_server"></a><dl>
<dt><b>SP_PROT_SSL2_SERVER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 2.0 server side. Superseded by SP_PROT_TLS1_SERVER.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.2 flags are mutually exclusive.</div>
<div> </div>
<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support ends.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_SSL2_CLIENT"></a><a id="sp_prot_ssl2_client"></a><dl>
<dt><b>SP_PROT_SSL2_CLIENT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 2.0 client side. Superseded by SP_PROT_TLS1_CLIENT.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.2 flags are mutually exclusive.</div>
<div> </div>
<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support ends.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_SSL3_SERVER"></a><a id="sp_prot_ssl3_server"></a><dl>
<dt><b>SP_PROT_SSL3_SERVER</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 3.0 server side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_SSL3_CLIENT"></a><a id="sp_prot_ssl3_client"></a><dl>
<dt><b>SP_PROT_SSL3_CLIENT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Secure Sockets Layer 3.0 client side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_SERVER"></a><a id="sp_prot_tls1_server"></a><dl>
<dt><b>SP_PROT_TLS1_SERVER</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.0 server side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_CLIENT"></a><a id="sp_prot_tls1_client"></a><dl>
<dt><b>SP_PROT_TLS1_CLIENT</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.0 client side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_0_SERVER"></a><a id="sp_prot_tls1_0_server"></a><dl>
<dt><b>SP_PROT_TLS1_0_SERVER</b></dt>
<dt>SP_PROT_TLS1_SERVER</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.0 server side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_0_CLIENT"></a><a id="sp_prot_tls1_0_client"></a><dl>
<dt><b>SP_PROT_TLS1_0_CLIENT</b></dt>
<dt>SP_PROT_TLS1_CLIENT</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.0 client side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_1_SERVER"></a><a id="sp_prot_tls1_1_server"></a><dl>
<dt><b>SP_PROT_TLS1_1_SERVER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.1 server side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_1_CLIENT"></a><a id="sp_prot_tls1_1_client"></a><dl>
<dt><b>SP_PROT_TLS1_1_CLIENT</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.1 client side.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_2_SERVER"></a><a id="sp_prot_tls1_2_server"></a><dl>
<dt><b>SP_PROT_TLS1_2_SERVER</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.2 server side.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.2 flags are mutually exclusive.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_2_CLIENT"></a><a id="sp_prot_tls1_2_client"></a><dl>
<dt><b>SP_PROT_TLS1_2_CLIENT</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.2 client side.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.2 flags are mutually exclusive.</div>
<div> </div>
</td>
</tr>
<tr>
 
<tr>
<td width="40%"><a id="SP_PROT_TLS1_3_SERVER"></a><a id="sp_prot_tls1_3_server"></a><dl>
<dt><b>SP_PROT_TLS1_3_SERVER</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.3 server side.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.2 flags are mutually exclusive.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_TLS1_3_CLIENT"></a><a id="sp_prot_tls1_3_client"></a><dl>
<dt><b>SP_PROT_TLS1_3_CLIENT</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Transport Layer Security 1.3 client side.

<div class="alert"><b>Important</b>  Secure Sockets Layer 2.0 and Transport Layer Security 1.3 flags are mutually exclusive.</div>
<div> </div>
</td>
</tr>
<tr>
 
<td width="40%"><a id="SP_PROT_DTLS_SERVER"></a><a id="sp_prot_dtls_server"></a><dl>
<dt><b>SP_PROT_DTLS_SERVER</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security server side.

<b>Windows 8 and Windows Server 2012:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS_CLIENT"></a><a id="sp_prot_dtls_client"></a><dl>
<dt><b>SP_PROT_DTLS_CLIENT</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security client side.

<b>Windows 8 and Windows Server 2012:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_0_SERVER"></a><a id="sp_prot_dtls1_0_server"></a><dl>
<dt><b>SP_PROT_DTLS1_0_SERVER</b></dt>
<dt>SP_PROT_DTLS1_SERVER</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.0 server side.

<b>Windows 8 and Windows Server 2012:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_0_CLIENT"></a><a id="sp_prot_dtls1_0_client"></a><dl>
<dt><b>SP_PROT_DTLS1_0_CLIENT</b></dt>
<dt>SP_PROT_DTLS1_CLIENT</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.0 client side.

<b>Windows 8 and Windows Server 2012:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_2_SERVER"></a><a id="sp_prot_dtls1_2_server"></a><dl>
<dt><b>SP_PROT_DTLS1_2_SERVER</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.2 server side.

<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_2_CLIENT"></a><a id="sp_prot_dtls1_2_client"></a><dl>
<dt><b>SP_PROT_DTLS1_2_CLIENT</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security 1.2 client side.

<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_X_SERVER"></a><a id="sp_prot_dtls1_x_server"></a><dl>
<dt><b>SP_PROT_DTLS1_X_SERVER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security all supported versions server side.

<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support added.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PROT_DTLS1_X_CLIENT"></a><a id="sp_prot_dtls1_x_client"></a><dl>
<dt><b>SP_PROT_DTLS1_X_CLIENT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Datagram Transport Layer Security all supported versions client side.

<b>Windows 10, version 1607 and Windows Server 2016.:  </b>Support added.

</td>
</tr>
</table>

### -field dwMinimumCipherStrength

Minimum bulk encryption cipher strength, in bits, allowed for connections.

If this member is zero, Schannel uses the system default. If this member is –1, only the SSL3/TLS MAC–only cipher suites (also known as <b>NULL</b> cipher) are enabled.

### -field dwMaximumCipherStrength

Maximum bulk encryption cipher strength, in bits, allowed for connections.

If this member is zero, Schannel uses the system default.

If this member is –1, only the SSL3/TLS MAC–only cipher suites (also known as <b>NULL</b> cipher) are enabled. In this case, <i>dwMinimumCipherStrength</i> must be set to –1.

### -field dwSessionLifespan

The number of milliseconds that Schannel keeps the session in its session cache. After this time has passed, any new connections between the client and the server require a new Schannel  session. Set the value of this member to zero to use the default value of 36000000 milliseconds (ten hours).

### -field dwFlags

Contains bit flags that control the behavior of Schannel. This member can be zero or a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_AUTO_CRED_VALIDATION"></a><a id="sch_cred_auto_cred_validation"></a><dl>
<dt><b>SCH_CRED_AUTO_CRED_VALIDATION</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Client only.

This flag is the opposite of SCH_CRED_MANUAL_CRED_VALIDATION and is part of the default behavior of Schannel.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_CACHE_ONLY_URL_RETRIEVAL_ON_CREATE"></a><a id="sch_cred_cache_only_url_retrieval_on_create"></a><dl>
<dt><b>SCH_CRED_CACHE_ONLY_URL_RETRIEVAL_ON_CREATE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Instruct Schannel to pass the CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL flag to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function when validating the specified credentials during a call to <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (Schannel)</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_DISABLE_RECONNECTS"></a><a id="sch_disable_reconnects"></a><dl>
<dt><b>SCH_CRED_DISABLE_RECONNECTS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Server only.

If this flag is set, then full handshakes performed with this credential will not allow reconnects. A cache entry is created, so the session can be made resumable later by using the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_IGNORE_NO_REVOCATION_CHECK"></a><a id="sch_cred_ignore_no_revocation_check"></a><dl>
<dt><b>SCH_CRED_IGNORE_NO_REVOCATION_CHECK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
When checking for revoked certificates, ignore CRYPT_E_NO_REVOCATION_CHECK errors. For  additional restrictions, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_IGNORE_REVOCATION_OFFLINE"></a><a id="sch_cred_ignore_revocation_offline"></a><dl>
<dt><b>SCH_CRED_IGNORE_REVOCATION_OFFLINE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
When checking for revoked certificates, ignore CRYPT_E_REVOCATION_OFFLINE errors. For additional restrictions, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_MANUAL_CRED_VALIDATION"></a><a id="sch_cred_manual_cred_validation"></a><dl>
<dt><b>SCH_CRED_MANUAL_CRED_VALIDATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Client only.

Prevent Schannel from validating the received server certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_NO_DEFAULT_CREDS"></a><a id="sch_cred_no_default_creds"></a><dl>
<dt><b>SCH_CRED_NO_DEFAULT_CREDS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Client only.

Prevent Schannel from attempting to automatically supply a certificate chain for client authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_NO_SERVERNAME_CHECK"></a><a id="sch_cred_no_servername_check"></a><dl>
<dt><b>SCH_CRED_NO_SERVERNAME_CHECK</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Client only.

Prevent Schannel from comparing the supplied target name with the subject names in <a href="/windows/desktop/SecGloss/s-gly">server certificates</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_NO_SYSTEM_MAPPER"></a><a id="sch_cred_no_system_mapper"></a><dl>
<dt><b>SCH_CRED_NO_SYSTEM_MAPPER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Server only.

Prevent Schannel from using the built-in system certificate mapping functions to map <a href="/windows/desktop/SecGloss/c-gly">client certificates</a> to a user account.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_REVOCATION_CHECK_CHAIN"></a><a id="sch_cred_revocation_check_chain"></a><dl>
<dt><b>SCH_CRED_REVOCATION_CHECK_CHAIN</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
When validating a certificate chain, check all certificates for revocation. For  additional restrictions, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT"></a><a id="sch_cred_revocation_check_chain_exclude_root"></a><dl>
<dt><b>SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
When validating a certificate chain, do not check the root for revocation. For  additional restrictions, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_REVOCATION_CHECK_END_CERT"></a><a id="sch_cred_revocation_check_end_cert"></a><dl>
<dt><b>SCH_CRED_REVOCATION_CHECK_END_CERT</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
When validating a certificate chain, check only the last certificate for revocation. For  additional restrictions, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_USE_DEFAULT_CREDS"></a><a id="sch_cred_use_default_creds"></a><dl>
<dt><b>SCH_CRED_USE_DEFAULT_CREDS</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Client only.

Schannel attempts to automatically supply a certificate chain for client authentication. This value is the opposite of SCH_CRED_NO_DEFAULT_CREDS.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_SEND_AUX_RECORD"></a><a id="sch_send_aux_record"></a><dl>
<dt><b>SCH_SEND_AUX_RECORD</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Instruct Schannel to split data to be encrypted into two separate records to counter weakness present in the SSL/TLS protocol when used with symmetric cipher suite using cipher block chaining mode. For more information, see <a href="https://support.microsoft.com/topic/ms12-006-vulnerability-in-ssl-tls-could-allow-information-disclosure-january-10-2012-41786996-65e1-ad9e-7536-fdc4017a81a1">Vulnerability in SSL/TLS Could Allow Information Disclosure</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP and Windows XP/2000:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_SEND_ROOT_CERT"></a><a id="sch_send_root_cert"></a><dl>
<dt><b>SCH_SEND_ROOT_CERT</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Schannel sends the root certificate as part of the certificate message.

<div class="alert"><b>Note</b>  The root certificate sent over the network by the Schannel client or server is not to be trusted. It should be validated against a trusted hash of the root certificate.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SCH_USE_STRONG_CRYPTO"></a><a id="sch_use_strong_crypto"></a><dl>
<dt><b>SCH_USE_STRONG_CRYPTO</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
Instructs Schannel to disable known weak cryptographic algorithms, cipher suites, and SSL/TLS protocol versions that may be otherwise enabled for better interoperability.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_USE_PRESHAREDKEY_ONLY"></a><a id="sch_use_presharedkey_only"></a><dl>
<dt><b>SCH_USE_PRESHAREDKEY_ONLY</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
Instructs Schannel to select only PSK cipher suites and disable all other cipher suites.

</td>
</tr>
</table>

### -field dwCredFormat

Kernel-mode Schannel supports the following values.

<b>Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP and Windows XP/2000:  </b>This flag is not supported and must be zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_FORMAT_CERT_HASH"></a><a id="sch_cred_format_cert_hash"></a><dl>
<dt><b>SCH_CRED_FORMAT_CERT_HASH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>paCred</b> member  of the <b>SCHANNEL_CRED</b> structure passed in must be a pointer to a byte array of length 20 that contains the certificate thumbprint. The certificate is assumed to be in the "MY" store of the local computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_FORMAT_CERT_HASH_STORE"></a><a id="sch_cred_format_cert_hash_store"></a><dl>
<dt><b>SCH_CRED_FORMAT_CERT_HASH_STORE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>paCred</b> member  of the <b>SCHANNEL_CRED</b> structure points to a <a href="/windows/desktop/api/schannel/ns-schannel-schannel_cert_hash_store">SCHANNEL_CERT_HASH_STORE</a> structure.

</td>
</tr>
</table>

## -remarks

The following certificate revocation flags are mutually exclusive.




<ul>
<li>SCH_CRED_REVOCATION_CHECK_CHAIN</li>
<li>SCH_CRED_REVOCATION_CHECK_END_CERT</li>
<li>SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</li>
</ul>



To customize certificate revocation error reporting for Schannel, use the following flags:

<ul>
<li>SCH_CRED_IGNORE_NO_REVOCATION_CHECK</li>
<li>SCH_CRED_IGNORE_REVOCATION_OFFLINE</li>
</ul>


When Schannel checks the revocation status of a certificate chain, these flags instruct it to ignore any CRYPT_E_NO_REVOCATION_CHECK and CRYPT_E_REVOCATION_OFFLINE errors, respectively. These flags are ignored if no certificate revocation flag is set.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querysecuritycontexttoken">QuerySecurityContextToken</a>
