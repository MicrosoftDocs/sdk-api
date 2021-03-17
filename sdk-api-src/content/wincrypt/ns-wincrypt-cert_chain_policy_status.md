---
UID: NS:wincrypt._CERT_CHAIN_POLICY_STATUS
title: CERT_CHAIN_POLICY_STATUS (wincrypt.h)
description: Holds certificate chain status information returned by the CertVerifyCertificateChainPolicy function when the certificate chains are validated.
helpviewer_keywords: ["*PCERT_CHAIN_POLICY_STATUS","CERT_CHAIN_POLICY_STATUS","CERT_CHAIN_POLICY_STATUS structure [Security]","CERT_E_CHAINING","CERT_E_CN_NO_MATCH","CERT_E_CRITICAL","CERT_E_EXPIRED","CERT_E_INVALID_NAME","CERT_E_INVALID_POLICY","CERT_E_PURPOSE","CERT_E_REVOCATION_FAILURE","CERT_E_REVOKED","CERT_E_ROLE","CERT_E_UNTRUSTEDROOT","CERT_E_UNTRUSTEDTESTROOT","CERT_E_VALIDITYPERIODNESTING","CERT_E_WRONG_USAGE","CRYPT_E_NO_REVOCATION_CHECK","CRYPT_E_REVOCATION_OFFLINE","CRYPT_E_REVOKED","PCERT_CHAIN_POLICY_STATUS","PCERT_CHAIN_POLICY_STATUS structure pointer [Security]","TRUST_E_BASIC_CONSTRAINTS","TRUST_E_CERT_SIGNATURE","_crypto2_cert_chain_policy_status","security.cert_chain_policy_status","wincrypt/CERT_CHAIN_POLICY_STATUS","wincrypt/PCERT_CHAIN_POLICY_STATUS"]
old-location: security\cert_chain_policy_status.htm
tech.root: security
ms.assetid: 599a09b6-fe9e-4489-99ae-8a88fa78a660
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_POLICY_STATUS, CERT_CHAIN_POLICY_STATUS, CERT_CHAIN_POLICY_STATUS structure [Security], CERT_E_CHAINING, CERT_E_CN_NO_MATCH, CERT_E_CRITICAL, CERT_E_EXPIRED, CERT_E_INVALID_NAME, CERT_E_INVALID_POLICY, CERT_E_PURPOSE, CERT_E_REVOCATION_FAILURE, CERT_E_REVOKED, CERT_E_ROLE, CERT_E_UNTRUSTEDROOT, CERT_E_UNTRUSTEDTESTROOT, CERT_E_VALIDITYPERIODNESTING, CERT_E_WRONG_USAGE, CRYPT_E_NO_REVOCATION_CHECK, CRYPT_E_REVOCATION_OFFLINE, CRYPT_E_REVOKED, PCERT_CHAIN_POLICY_STATUS, PCERT_CHAIN_POLICY_STATUS structure pointer [Security], TRUST_E_BASIC_CONSTRAINTS, TRUST_E_CERT_SIGNATURE, _crypto2_cert_chain_policy_status, security.cert_chain_policy_status, wincrypt/CERT_CHAIN_POLICY_STATUS, wincrypt/PCERT_CHAIN_POLICY_STATUS'
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
req.typenames: CERT_CHAIN_POLICY_STATUS, *PCERT_CHAIN_POLICY_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_POLICY_STATUS
 - wincrypt/_CERT_CHAIN_POLICY_STATUS
 - PCERT_CHAIN_POLICY_STATUS
 - wincrypt/PCERT_CHAIN_POLICY_STATUS
 - CERT_CHAIN_POLICY_STATUS
 - wincrypt/CERT_CHAIN_POLICY_STATUS
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
 - CERT_CHAIN_POLICY_STATUS
---

# CERT_CHAIN_POLICY_STATUS structure


## -description

The <b>CERT_CHAIN_POLICY_STATUS</b> structure holds certificate chain status information returned by 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function when the certificate chains are validated.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwError

A value that indicates that an error or invalid condition was encountered during the  validation process. The values of this member are specific to the policy type as specified by the value of the   <i>pszPolicyOID</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function.


Base Policy errors (<b>CERT_CHAIN_POLICY_BASE</b>)




<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_E_CERT_SIGNATURE"></a><a id="trust_e_cert_signature"></a><dl>
<dt><b>TRUST_E_CERT_SIGNATURE</b></dt>
<dt>0x80096004L</dt>
</dl>
</td>
<td width="60%">
The signature of the certificate cannot be verified.


</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_E_REVOKED"></a><a id="crypt_e_revoked"></a><dl>
<dt><b>CRYPT_E_REVOKED</b></dt>
<dt>0x80092010L</dt>
</dl>
</td>
<td width="60%">
The certificate or signature has been revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_UNTRUSTEDROOT"></a><a id="cert_e_untrustedroot"></a><dl>
<dt><b>CERT_E_UNTRUSTEDROOT</b></dt>
<dt>0x800B0109L</dt>
</dl>
</td>
<td width="60%">
A certification chain processed correctly but terminated in a root certificate that is not trusted by the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_UNTRUSTEDTESTROOT"></a><a id="cert_e_untrustedtestroot"></a><dl>
<dt><b>CERT_E_UNTRUSTEDTESTROOT</b></dt>
<dt>0x800B010DL</dt>
</dl>
</td>
<td width="60%">
The root certificate is a testing certificate, and policy settings disallow test certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_CHAINING"></a><a id="cert_e_chaining"></a><dl>
<dt><b>CERT_E_CHAINING</b></dt>
<dt>0x800B010AL</dt>
</dl>
</td>
<td width="60%">
A chain of certificates was not correctly created.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_WRONG_USAGE"></a><a id="cert_e_wrong_usage"></a><dl>
<dt><b>CERT_E_WRONG_USAGE</b></dt>
<dt>0x800B0110L</dt>
</dl>
</td>
<td width="60%">
The certificate is not valid for the requested usage.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_EXPIRED"></a><a id="cert_e_expired"></a><dl>
<dt><b>CERT_E_EXPIRED</b></dt>
<dt>0x800B0101L</dt>
</dl>
</td>
<td width="60%">
A required certificate is not within its validity period.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_INVALID_NAME"></a><a id="cert_e_invalid_name"></a><dl>
<dt><b>CERT_E_INVALID_NAME</b></dt>
<dt>0x800B0114L</dt>
</dl>
</td>
<td width="60%">
The certificate has an invalid name. Either the name is not included in the permitted list, or it is explicitly excluded.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_INVALID_POLICY"></a><a id="cert_e_invalid_policy"></a><dl>
<dt><b>CERT_E_INVALID_POLICY</b></dt>
<dt>0x800B0113L</dt>
</dl>
</td>
<td width="60%">
The certificate has an invalid policy.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_E_BASIC_CONSTRAINTS"></a><a id="trust_e_basic_constraints"></a><dl>
<dt><b>TRUST_E_BASIC_CONSTRAINTS</b></dt>
<dt>0x80096019L</dt>
</dl>
</td>
<td width="60%">
The basic constraints of the certificate are not valid, or they are missing.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_CRITICAL"></a><a id="cert_e_critical"></a><dl>
<dt><b>CERT_E_CRITICAL</b></dt>
<dt>0x800B0105L</dt>
</dl>
</td>
<td width="60%">
The certificate is being used for a purpose other than the purpose specified by its CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_VALIDITYPERIODNESTING"></a><a id="cert_e_validityperiodnesting"></a><dl>
<dt><b>CERT_E_VALIDITYPERIODNESTING</b></dt>
<dt>0x800B0102L</dt>
</dl>
</td>
<td width="60%">
The validity periods of the certification chain do not nest correctly.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_E_NO_REVOCATION_CHECK"></a><a id="crypt_e_no_revocation_check"></a><dl>
<dt><b>CRYPT_E_NO_REVOCATION_CHECK</b></dt>
<dt>0x80092012L</dt>
</dl>
</td>
<td width="60%">
The revocation function was unable to check revocation for the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_E_REVOCATION_OFFLINE"></a><a id="crypt_e_revocation_offline"></a><dl>
<dt><b>CRYPT_E_REVOCATION_OFFLINE</b></dt>
<dt>0x80092013L</dt>
</dl>
</td>
<td width="60%">
The revocation function was unable to check revocation because the revocation server was offline.

</td>
</tr>
</table>
 


Basic Constraints Policy errors (<b>CERT_CHAIN_POLICY_BASIC_CONSTRAINTS</b>).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_E_BASIC_CONSTRAINTS"></a><a id="trust_e_basic_constraints"></a><dl>
<dt><b>TRUST_E_BASIC_CONSTRAINTS</b></dt>
<dt>0x80096019L</dt>
</dl>
</td>
<td width="60%">
The basic constraints of the certificate are not valid, or they are missing.

</td>
</tr>
</table>
 


Authenticode Policy errors (<b>CERT_CHAIN_POLICY_AUTHENTICODE</b> and <b>CERT_CHAIN_POLICY_AUTHENTICODE_TS</b>).

These errors are in addition to the Base Policy errors.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_E_PURPOSE"></a><a id="cert_e_purpose"></a><dl>
<dt><b>CERT_E_PURPOSE</b></dt>
<dt>0x800B0106L</dt>
</dl>
</td>
<td width="60%">
The certificate is being used for a purpose other than one specified by the issuing CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_REVOKED"></a><a id="cert_e_revoked"></a><dl>
<dt><b>CERT_E_REVOKED</b></dt>
<dt>0x800B010CL</dt>
</dl>
</td>
<td width="60%">
The certificate has been explicitly revoked by the issuer.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_REVOCATION_FAILURE"></a><a id="cert_e_revocation_failure"></a><dl>
<dt><b>CERT_E_REVOCATION_FAILURE</b></dt>
<dt>0x800B010EL</dt>
</dl>
</td>
<td width="60%">
The revocation process could not continue, and the certificate could not be checked.

</td>
</tr>
</table>
 


SSL Policy errors (<b>CERT_CHAIN_POLICY_SSL</b>).

These errors are in addition to the Base Policy errors.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_E_UNTRUSTEDROOT"></a><a id="cert_e_untrustedroot"></a><dl>
<dt><b>CERT_E_UNTRUSTEDROOT</b></dt>
<dt>0x800B0109L</dt>
</dl>
</td>
<td width="60%">
A certification chain processed correctly but terminated in a root certificate that is not trusted by the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_CN_NO_MATCH"></a><a id="cert_e_cn_no_match"></a><dl>
<dt><b>CERT_E_CN_NO_MATCH</b></dt>
<dt>0x800B010FL</dt>
</dl>
</td>
<td width="60%">
The certificate's CN name does not match the passed value.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_PURPOSE"></a><a id="cert_e_purpose"></a><dl>
<dt><b>CERT_E_PURPOSE</b></dt>
<dt>0x800B0106L</dt>
</dl>
</td>
<td width="60%">
The certificate is being used for a purpose other than the purposes specified by its CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_ROLE"></a><a id="cert_e_role"></a><dl>
<dt><b>CERT_E_ROLE</b></dt>
<dt>0x800B0103L</dt>
</dl>
</td>
<td width="60%">
A certificate that can only be used as an end-entity is being used as a CA or vice versa.

</td>
</tr>
</table>
 


Microsoft Root Policy errors (<b>CERT_CHAIN_POLICY_MICROSOFT_ROOT</b>).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_E_UNTRUSTEDROOT"></a><a id="cert_e_untrustedroot"></a><dl>
<dt><b>CERT_E_UNTRUSTEDROOT</b></dt>
<dt>0x800B0109L</dt>
</dl>
</td>
<td width="60%">
A certification chain processed correctly but terminated in a root certificate that is not trusted by the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a>.

</td>
</tr>
</table>
 


EV Policy errors.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_E_CHAINING"></a><a id="cert_e_chaining"></a><dl>
<dt><b>CERT_E_CHAINING</b></dt>
<dt>0x800B010AL</dt>
</dl>
</td>
<td width="60%">
The certificate chain to a trusted root authority could not be built.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_E_WRONG_USAGE"></a><a id="cert_e_wrong_usage"></a><dl>
<dt><b>CERT_E_WRONG_USAGE</b></dt>
<dt>0x800B0110L</dt>
</dl>
</td>
<td width="60%">
The certificate is not valid for the requested usage.

</td>
</tr>
</table>

### -field lChainIndex

Index that indicates the chain in which an error or condition that is not valid was found. For more information, see Remarks.

### -field lElementIndex

Index that indicates the element in a chain where an error or condition that is not valid was found. For more information, see Remarks.

### -field pvExtraPolicyStatus

A pointer to a structure. The structure type is determined by the value of the <b>pszPolicyOID</b> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function. In addition to <b>dwError</b> errors, policy OID–specific extra status can also be returned here to provide additional chain status information. This pointer can be optionally set to point to an 
<a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_extra_cert_chain_policy_status">AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS</a> structure.

## -remarks

If both <b>lChainIndex</b> and <b>lElementIndex</b> are set to –1, the error or condition that is not valid applies to the whole chain context. If only <b>lElementIndex</b> is set to –1, the error or condition that is not valid applies to the chain indexed by <b>lChainIndex</b>. Otherwise, the error or condition that is not valid applies to the certificate element at pChainContext-&gt;rgpChain[<b>lChainIndex</b>]-&gt;rgpElement[<b>lElementIndex</b>].