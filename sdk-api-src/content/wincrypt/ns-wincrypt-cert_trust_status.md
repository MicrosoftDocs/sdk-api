---
UID: NS:wincrypt._CERT_TRUST_STATUS
title: CERT_TRUST_STATUS (wincrypt.h)
description: Contains trust information about a certificate in a certificate chain, summary trust information about a simple chain of certificates, or summary information about an array of simple chains.
helpviewer_keywords: ["*PCERT_TRUST_STATUS","CERT_TRUST_CTL_IS_NOT_SIGNATURE_VALID","CERT_TRUST_CTL_IS_NOT_TIME_VALID","CERT_TRUST_CTL_IS_NOT_VALID_FOR_USAGE","CERT_TRUST_HAS_CRL_VALIDITY_EXTENDED","CERT_TRUST_HAS_EXACT_MATCH_ISSUER","CERT_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT","CERT_TRUST_HAS_ISSUANCE_CHAIN_POLICY","CERT_TRUST_HAS_KEY_MATCH_ISSUER","CERT_TRUST_HAS_NAME_MATCH_ISSUER","CERT_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT","CERT_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT","CERT_TRUST_HAS_NOT_SUPPORTED_CRITICAL_EXT","CERT_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT","CERT_TRUST_HAS_PREFERRED_ISSUER","CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS","CERT_TRUST_HAS_WEAK_SIGNATURE","CERT_TRUST_INVALID_BASIC_CONSTRAINTS","CERT_TRUST_INVALID_EXTENSION","CERT_TRUST_INVALID_NAME_CONSTRAINTS","CERT_TRUST_INVALID_POLICY_CONSTRAINTS","CERT_TRUST_IS_CA_TRUSTED","CERT_TRUST_IS_COMPLEX_CHAIN","CERT_TRUST_IS_CYCLIC","CERT_TRUST_IS_EXPLICIT_DISTRUST","CERT_TRUST_IS_FROM_EXCLUSIVE_TRUST_STORE","CERT_TRUST_IS_NOT_SIGNATURE_VALID","CERT_TRUST_IS_NOT_TIME_VALID","CERT_TRUST_IS_NOT_VALID_FOR_USAGE","CERT_TRUST_IS_OFFLINE_REVOCATION","CERT_TRUST_IS_PARTIAL_CHAIN","CERT_TRUST_IS_PEER_TRUSTED","CERT_TRUST_IS_REVOKED","CERT_TRUST_IS_SELF_SIGNED","CERT_TRUST_IS_UNTRUSTED_ROOT","CERT_TRUST_NO_ERROR","CERT_TRUST_NO_ISSUANCE_CHAIN_POLICY","CERT_TRUST_REVOCATION_STATUS_UNKNOWN","CERT_TRUST_STATUS","CERT_TRUST_STATUS structure [Security]","PCERT_TRUST_STATUS","PCERT_TRUST_STATUS structure pointer [Security]","_crypto2_cert_trust_status","security.cert_trust_status","wincrypt/CERT_TRUST_STATUS","wincrypt/PCERT_TRUST_STATUS"]
old-location: security\cert_trust_status.htm
tech.root: security
ms.assetid: af1e1db2-7b53-4491-8317-4abf3568fb03
ms.date: 12/05/2018
ms.keywords: '*PCERT_TRUST_STATUS, CERT_TRUST_CTL_IS_NOT_SIGNATURE_VALID, CERT_TRUST_CTL_IS_NOT_TIME_VALID, CERT_TRUST_CTL_IS_NOT_VALID_FOR_USAGE, CERT_TRUST_HAS_CRL_VALIDITY_EXTENDED, CERT_TRUST_HAS_EXACT_MATCH_ISSUER, CERT_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT, CERT_TRUST_HAS_ISSUANCE_CHAIN_POLICY, CERT_TRUST_HAS_KEY_MATCH_ISSUER, CERT_TRUST_HAS_NAME_MATCH_ISSUER, CERT_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT, CERT_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT, CERT_TRUST_HAS_NOT_SUPPORTED_CRITICAL_EXT, CERT_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT, CERT_TRUST_HAS_PREFERRED_ISSUER, CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS, CERT_TRUST_HAS_WEAK_SIGNATURE, CERT_TRUST_INVALID_BASIC_CONSTRAINTS, CERT_TRUST_INVALID_EXTENSION, CERT_TRUST_INVALID_NAME_CONSTRAINTS, CERT_TRUST_INVALID_POLICY_CONSTRAINTS, CERT_TRUST_IS_CA_TRUSTED, CERT_TRUST_IS_COMPLEX_CHAIN, CERT_TRUST_IS_CYCLIC, CERT_TRUST_IS_EXPLICIT_DISTRUST, CERT_TRUST_IS_FROM_EXCLUSIVE_TRUST_STORE, CERT_TRUST_IS_NOT_SIGNATURE_VALID, CERT_TRUST_IS_NOT_TIME_VALID, CERT_TRUST_IS_NOT_VALID_FOR_USAGE, CERT_TRUST_IS_OFFLINE_REVOCATION, CERT_TRUST_IS_PARTIAL_CHAIN, CERT_TRUST_IS_PEER_TRUSTED, CERT_TRUST_IS_REVOKED, CERT_TRUST_IS_SELF_SIGNED, CERT_TRUST_IS_UNTRUSTED_ROOT, CERT_TRUST_NO_ERROR, CERT_TRUST_NO_ISSUANCE_CHAIN_POLICY, CERT_TRUST_REVOCATION_STATUS_UNKNOWN, CERT_TRUST_STATUS, CERT_TRUST_STATUS structure [Security], PCERT_TRUST_STATUS, PCERT_TRUST_STATUS structure pointer [Security], _crypto2_cert_trust_status, security.cert_trust_status, wincrypt/CERT_TRUST_STATUS, wincrypt/PCERT_TRUST_STATUS'
req.header: wincrypt.h
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
req.typenames: CERT_TRUST_STATUS, *PCERT_TRUST_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_TRUST_STATUS
 - wincrypt/_CERT_TRUST_STATUS
 - PCERT_TRUST_STATUS
 - wincrypt/PCERT_TRUST_STATUS
 - CERT_TRUST_STATUS
 - wincrypt/CERT_TRUST_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_TRUST_STATUS
---

# CERT_TRUST_STATUS structure


## -description

The <b>CERT_TRUST_STATUS</b> structure contains trust information about a certificate in a certificate chain, summary trust information about a simple chain of certificates, or summary information about an array of simple chains.

## -struct-fields

### -field dwErrorStatus

dwErrorStatus is a bitmask of the following error codes defined for certificates and chains. 




						
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_NO_ERROR"></a><a id="cert_trust_no_error"></a><dl>
<dt><b>CERT_TRUST_NO_ERROR</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
No error found for this certificate or chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_NOT_TIME_VALID"></a><a id="cert_trust_is_not_time_valid"></a><dl>
<dt><b>CERT_TRUST_IS_NOT_TIME_VALID</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This certificate or one of the certificates in the certificate chain is not time valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_REVOKED"></a><a id="cert_trust_is_revoked"></a><dl>
<dt><b>CERT_TRUST_IS_REVOKED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Trust for this certificate or one of the certificates in the certificate chain has been revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_NOT_SIGNATURE_VALID"></a><a id="cert_trust_is_not_signature_valid"></a><dl>
<dt><b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain does not have a valid signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_NOT_VALID_FOR_USAGE"></a><a id="cert_trust_is_not_valid_for_usage"></a><dl>
<dt><b>CERT_TRUST_IS_NOT_VALID_FOR_USAGE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The certificate or certificate chain is not valid for its proposed usage.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_UNTRUSTED_ROOT"></a><a id="cert_trust_is_untrusted_root"></a><dl>
<dt><b>CERT_TRUST_IS_UNTRUSTED_ROOT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The certificate or certificate chain is based on an untrusted root.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_REVOCATION_STATUS_UNKNOWN"></a><a id="cert_trust_revocation_status_unknown"></a><dl>
<dt><b>CERT_TRUST_REVOCATION_STATUS_UNKNOWN</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The revocation status of the certificate or one of the certificates in the certificate chain is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_CYCLIC"></a><a id="cert_trust_is_cyclic"></a><dl>
<dt><b>CERT_TRUST_IS_CYCLIC</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
One of the certificates in the chain was issued by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> that the original certificate had certified.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_INVALID_EXTENSION"></a><a id="cert_trust_invalid_extension"></a><dl>
<dt><b>CERT_TRUST_INVALID_EXTENSION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
One of the certificates has an extension that is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_INVALID_POLICY_CONSTRAINTS"></a><a id="cert_trust_invalid_policy_constraints"></a><dl>
<dt><b>CERT_TRUST_INVALID_POLICY_CONSTRAINTS</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_INVALID_BASIC_CONSTRAINTS"></a><a id="cert_trust_invalid_basic_constraints"></a><dl>
<dt><b>CERT_TRUST_INVALID_BASIC_CONSTRAINTS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_INVALID_NAME_CONSTRAINTS"></a><a id="cert_trust_invalid_name_constraints"></a><dl>
<dt><b>CERT_TRUST_INVALID_NAME_CONSTRAINTS</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></a><a id="cert_trust_has_not_supported_name_constraint"></a><dl>
<dt><b>CERT_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields. The minimum and maximum fields are not supported. Thus minimum must always be zero and maximum must always be absent. Only UPN is supported for an Other Name. The following alternative name choices are not supported:

<ul>
<li>X400 Address</li>
<li>EDI Party Name</li>
<li>Registered Id</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></a><a id="cert_trust_has_not_defined_name_constraint"></a><dl>
<dt><b>CERT_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a name constraints extension and a name constraint is missing for one of the name choices in the end certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></a><a id="cert_trust_has_not_permitted_name_constraint"></a><dl>
<dt><b>CERT_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></a><a id="cert_trust_has_excluded_name_constraint"></a><dl>
<dt><b>CERT_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_OFFLINE_REVOCATION"></a><a id="cert_trust_is_offline_revocation"></a><dl>
<dt><b>CERT_TRUST_IS_OFFLINE_REVOCATION</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_NO_ISSUANCE_CHAIN_POLICY"></a><a id="cert_trust_no_issuance_chain_policy"></a><dl>
<dt><b>CERT_TRUST_NO_ISSUANCE_CHAIN_POLICY</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The end certificate does not have any resultant issuance policies, and one of the issuing <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> certificates has a policy constraints extension requiring it.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_EXPLICIT_DISTRUST"></a><a id="cert_trust_is_explicit_distrust"></a><dl>
<dt><b>CERT_TRUST_IS_EXPLICIT_DISTRUST</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The certificate is explicitly distrusted.

<b>Windows Vista and Windows Server 2008:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_NOT_SUPPORTED_CRITICAL_EXT"></a><a id="cert_trust_has_not_supported_critical_ext"></a><dl>
<dt><b>CERT_TRUST_HAS_NOT_SUPPORTED_CRITICAL_EXT</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
The certificate does not support a critical extension.

<b>Windows Vista and Windows Server 2008:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_WEAK_SIGNATURE"></a><a id="cert_trust_has_weak_signature"></a><dl>
<dt><b>CERT_TRUST_HAS_WEAK_SIGNATURE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The certificate has not been strong signed. Typically this indicates that the MD2 or MD5 hashing algorithms were used to create a hash of the certificate.

<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>
 


The following codes are defined for chains only.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_PARTIAL_CHAIN"></a><a id="cert_trust_is_partial_chain"></a><dl>
<dt><b>CERT_TRUST_IS_PARTIAL_CHAIN</b></dt>
<dt> 0x00010000</dt>
</dl>
</td>
<td width="60%">
The certificate chain is not complete.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_CTL_IS_NOT_TIME_VALID"></a><a id="cert_trust_ctl_is_not_time_valid"></a><dl>
<dt><b>CERT_TRUST_CTL_IS_NOT_TIME_VALID</b></dt>
<dt> 0x00020000</dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) used to create this chain was not time valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></a><a id="cert_trust_ctl_is_not_signature_valid"></a><dl>
<dt><b>CERT_TRUST_CTL_IS_NOT_SIGNATURE_VALID</b></dt>
<dt> 0x00040000</dt>
</dl>
</td>
<td width="60%">
A CTL used to create this chain did not have a valid signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></a><a id="cert_trust_ctl_is_not_valid_for_usage"></a><dl>
<dt><b>CERT_TRUST_CTL_IS_NOT_VALID_FOR_USAGE</b></dt>
<dt> 0x00080000</dt>
</dl>
</td>
<td width="60%">
A CTL used to create this chain is not valid for this usage.

</td>
</tr>
</table>

### -field dwInfoStatus

The following information status codes are defined.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_EXACT_MATCH_ISSUER"></a><a id="cert_trust_has_exact_match_issuer"></a><dl>
<dt><b>CERT_TRUST_HAS_EXACT_MATCH_ISSUER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
An exact match issuer certificate has been found for this certificate. This status code applies to certificates only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_KEY_MATCH_ISSUER"></a><a id="cert_trust_has_key_match_issuer"></a><dl>
<dt><b>CERT_TRUST_HAS_KEY_MATCH_ISSUER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
A key match issuer certificate has been found for this certificate. This status code applies to certificates only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_NAME_MATCH_ISSUER"></a><a id="cert_trust_has_name_match_issuer"></a><dl>
<dt><b>CERT_TRUST_HAS_NAME_MATCH_ISSUER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
A name match issuer certificate has been found for this certificate. This status code applies to certificates only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_SELF_SIGNED"></a><a id="cert_trust_is_self_signed"></a><dl>
<dt><b>CERT_TRUST_IS_SELF_SIGNED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
This certificate is self-signed. This status code applies to certificates only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_PREFERRED_ISSUER"></a><a id="cert_trust_has_preferred_issuer"></a><dl>
<dt><b>CERT_TRUST_HAS_PREFERRED_ISSUER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The certificate or chain has a preferred issuer. This status code applies to certificates and chains.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_ISSUANCE_CHAIN_POLICY"></a><a id="cert_trust_has_issuance_chain_policy"></a><dl>
<dt><b>CERT_TRUST_HAS_ISSUANCE_CHAIN_POLICY</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
An issuance chain policy exists. This status code applies to certificates and chains.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS"></a><a id="cert_trust_has_valid_name_constraints"></a><dl>
<dt><b>CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
A valid name constraints for all namespaces, including UPN. This status code applies to certificates and chains.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_PEER_TRUSTED"></a><a id="cert_trust_is_peer_trusted"></a><dl>
<dt><b>CERT_TRUST_IS_PEER_TRUSTED</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
This certificate is peer trusted. This status code applies to certificates only.

<b>Windows Vista and Windows Server 2008:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_HAS_CRL_VALIDITY_EXTENDED"></a><a id="cert_trust_has_crl_validity_extended"></a><dl>
<dt><b>CERT_TRUST_HAS_CRL_VALIDITY_EXTENDED</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
This certificate's <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) validity has been extended. This status code applies to certificates only.

<b>Windows Vista and Windows Server 2008:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_FROM_EXCLUSIVE_TRUST_STORE"></a><a id="cert_trust_is_from_exclusive_trust_store"></a><dl>
<dt><b>CERT_TRUST_IS_FROM_EXCLUSIVE_TRUST_STORE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The certificate was found in either a store pointed to by the  <b>hExclusiveRoot</b> or <b>hExclusiveTrustedPeople</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_engine_config">CERT_CHAIN_ENGINE_CONFIG</a> structure.

<b>Windows 7 and Windows Server 2008 R2:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_COMPLEX_CHAIN"></a><a id="cert_trust_is_complex_chain"></a><dl>
<dt><b>CERT_TRUST_IS_COMPLEX_CHAIN</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The certificate chain created is a complex chain. This status code applies to chains only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_TRUST_IS_CA_TRUSTED"></a><a id="cert_trust_is_ca_trusted"></a><dl>
<dt><b>CERT_TRUST_IS_CA_TRUSTED</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
A non-self-signed intermediate CA certificate was found in the store pointed to  by the <b>hExclusiveRoot</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_engine_config">CERT_CHAIN_ENGINE_CONFIG</a> structure. The CA certificate is treated as a trust anchor for the certificate chain. This flag will only be set if the <b>CERT_CHAIN_EXCLUSIVE_ENABLE_CA_FLAG</b> value is set in the <b>dwExclusiveFlags</b> member of the <b>CERT_CHAIN_ENGINE_CONFIG</b> structure.

If this flag is set, the <b>CERT_TRUST_IS_SELF_SIGNED</b> and the <b>CERT_TRUST_IS_PARTIAL_CHAIN</b><b>dwErrorStatus</b> flags will not be set.

<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_engine_config">CERT_CHAIN_ENGINE_CONFIG</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_simple_chain">CERT_SIMPLE_CHAIN</a>
