---
UID: NS:schannel._SCH_CREDENTIALS
title: SCH_CREDENTIALS
ms.date: 7/25/2022
targetos: Windows
description: Contains the data for an Schannel credential. (SCH_CREDENTIALS)
tech.root: security
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: schannel.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 1809 [desktop apps only]
req.target-type: Windows
req.typenames: SCH_CREDENTIALS, *PSCH_CREDENTIALS
req.umdf-ver: 
req.unicode-ansi: 
ms.keywords: 'SCH_CREDENTIALS, SCH_CREDENTIALS structure, PSCH_CREDENTIALS~,PSCHANNEL_CRED structure pointer [Security], SCHANNEL_CRED,SCH_CREDENTIALS structure [Security], SCH_CREDENTIALS, SCH_CREDENTIALS structure [Security],SCH_CRED_AUTO_CRED_VALIDATION, SCH_CRED_CACHE_ONLY_URL_RETRIEVAL_ON_CREATE, SCH_CRED_FORMAT_CERT_HASH, SCH_CRED_FORMAT_CERT_HASH_STORE, SCH_CRED_IGNORE_NO_REVOCATION_CHECK, SCH_CRED_IGNORE_REVOCATION_OFFLINE, SCH_CRED_MANUAL_CRED_VALIDATION, SCH_CRED_NO_DEFAULT_CREDS, SCH_CRED_NO_SERVERNAME_CHECK, SCH_CRED_NO_SYSTEM_MAPPER, SCH_CRED_REVOCATION_CHECK_CHAIN, SCH_CRED_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, SCH_CRED_REVOCATION_CHECK_END_CERT, SCH_CRED_USE_DEFAULT_CREDS, SCH_DISABLE_RECONNECTS, SCH_SEND_AUX_RECORD, SCH_SEND_ROOT_CERT, SCH_USE_PRESHAREDKEY_ONLY, SCH_USE_STRONG_CRYPTO, SP_PROT_DTLS1_0_CLIENT, SP_PROT_DTLS1_0_SERVER, SP_PROT_DTLS1_2_CLIENT, SP_PROT_DTLS1_2_SERVER, SP_PROT_DTLS1_X_CLIENT, SP_PROT_DTLS1_X_SERVER, SP_PROT_DTLS_CLIENT, SP_PROT_DTLS_SERVER, SP_PROT_PCT1_CLIENT, SP_PROT_PCT1_SERVER, SP_PROT_SSL2_CLIENT, SP_PROT_SSL2_SERVER, SP_PROT_SSL3_CLIENT, SP_PROT_SSL3_SERVER, SP_PROT_TLS1_0_CLIENT, SP_PROT_TLS1_0_SERVER, SP_PROT_TLS1_1_CLIENT, SP_PROT_TLS1_1_SERVER, SP_PROT_TLS1_2_CLIENT, SP_PROT_TLS1_2_SERVER, SP_PROT_TLS1_CLIENT, SP_PROT_TLS1_SERVER, _ssp_sch_credentials, schannel/PSCH_CREDENTIALS, schannel/sch_credentials, security.sch_credentials'
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - schannel.h
api_name:
 - _SCH_CREDENTIALS
 - SCH_CREDENTIALS
f1_keywords:
 - _SCH_CREDENTIALS
 - schannel/_SCH_CREDENTIALS
 - PSCH_CREDENTIALS
 - schannel/PSCH_CREDENTIALS
 - SCH_CREDENTIALS
 - schannel/SCH_CREDENTIALS
dev_langs:
 - c++
---

## -description

The SCH_CREDENTIALS structure contains initialization information for an Schannel credential.

## -struct-fields

### -field dwVersion

Set to SCH_CREDENTIALS_VERSION.

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
The <b>paCred</b> member  of the <b>SCH_CREDENTIALS</b> structure passed in must be a pointer to a byte array of length 20 that contains the certificate thumbprint. The certificate is assumed to be in the "MY" store of the local computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SCH_CRED_FORMAT_CERT_HASH_STORE"></a><a id="sch_cred_format_cert_hash_store"></a><dl>
<dt><b>SCH_CRED_FORMAT_CERT_HASH_STORE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>paCred</b> member  of the <b>SCH_CREDENTIALS</b> structure points to a <a href="/windows/desktop/api/schannel/ns-schannel-schannel_cert_hash_store">SCHANNEL_CERT_HASH_STORE</a> structure.

</td>
</tr>
</table>

### -field cCreds

The number of structures in the paCred array.

### -field paCred

An array of pointers to CERT_CONTEXT structures. Each pointer specifies a certificate that contains a private key to be used in authenticating the application. 

Client applications often pass in an empty list and either depend on Schannel to find an appropriate certificate or create a certificate later if needed.

### -field hRootStore

*Optional.* Valid for server applications only. Handle to a certificate store that contains self-signed root certificates for certification authorities (CAs) trusted by the application. This member is used only by server-side applications that require client authentication.

### -field cMappers

Reserved.

### -field aphMappers

Reserved.

### -field dwSessionLifespan

The number of milliseconds that Schannel keeps the session in its session cache. After this time has passed, any new connections between the client and the server require a new Schannel session. Set the value of this member to zero to use the default value of 36000000 milliseconds (ten hours).

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
<td width="40%"><a id="SCH_CRED_DISABLE_RECONNECTS"></a><a id="sch_cred_disable_reconnects"></a><dl>
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

### -field cTlsParameters

The count of entries in the pTlsParameters array.

It is an error to specify more than SCH_CRED_MAX_SUPPORTED_PARAMETERS.

### -field pTlsParameters

Array of pointers to the [TLS_PARAMETERS](/windows/win32/api/schannel/ns-schannel-tls_parameters) structures that indicate TLS parameter restrictions, if any. If no restrictions are specified, the system defaults are used. It is recommended that applications rely on the system defaults.

It is an error to include more than one [TLS_PARAMETERS](/windows/win32/api/schannel/ns-schannel-tls_parameters) structure with cAlpnIds == 0 and rgstrAlpnIds == NULL.

## -remarks

To use the SCH_CREDENTIALS structure, define SCHANNEL_USE_BLACKLISTS along with UNICODE_STRING and PUNICODE_STRING. Alternatively, include Ntdef.h, SubAuth.h or Winternl.h.

## -see-also

[CRYPTO_SETTINGS](ns-schannel-crypto_settings.md)

[TLS_PARAMETERS](ns-schannel-tls_parameters.md)
