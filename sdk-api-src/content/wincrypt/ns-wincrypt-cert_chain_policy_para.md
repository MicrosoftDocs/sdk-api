---
UID: NS:wincrypt._CERT_CHAIN_POLICY_PARA
title: CERT_CHAIN_POLICY_PARA (wincrypt.h)
description: Contains information used in CertVerifyCertificateChainPolicy to establish policy criteria for the verification of certificate chains.
helpviewer_keywords: ["*PCERT_CHAIN_POLICY_PARA","BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_CA_FLAG","BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_END_ENTITY_FLAG","CERT_CHAIN_POLICY_ALLOW_TESTROOT_FLAG","CERT_CHAIN_POLICY_ALLOW_UNKNOWN_CA_FLAG","CERT_CHAIN_POLICY_IGNORE_ALL_NOT_TIME_VALID_FLAGS","CERT_CHAIN_POLICY_IGNORE_ALL_REV_UNKNOWN_FLAGS","CERT_CHAIN_POLICY_IGNORE_CA_REV_UNKNOWN_FLAG","CERT_CHAIN_POLICY_IGNORE_CTL_NOT_TIME_VALID_FLAG","CERT_CHAIN_POLICY_IGNORE_CTL_SIGNER_REV_UNKNOWN_FLAG","CERT_CHAIN_POLICY_IGNORE_END_REV_UNKNOWN_FLAG","CERT_CHAIN_POLICY_IGNORE_INVALID_BASIC_CONSTRAINTS_FLAG","CERT_CHAIN_POLICY_IGNORE_INVALID_NAME_FLAG","CERT_CHAIN_POLICY_IGNORE_INVALID_POLICY_FLAG","CERT_CHAIN_POLICY_IGNORE_NOT_SUPPORTED_CRITICAL_EXT_FLAG","CERT_CHAIN_POLICY_IGNORE_NOT_TIME_NESTED_FLAG","CERT_CHAIN_POLICY_IGNORE_NOT_TIME_VALID_FLAG","CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG","CERT_CHAIN_POLICY_IGNORE_ROOT_REV_UNKNOWN_FLAG","CERT_CHAIN_POLICY_IGNORE_WRONG_USAGE_FLAG","CERT_CHAIN_POLICY_PARA","CERT_CHAIN_POLICY_PARA structure [Security]","CERT_CHAIN_POLICY_TRUST_TESTROOT_FLAG","MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG","PCERT_CHAIN_POLICY_PARA","PCERT_CHAIN_POLICY_PARA structure pointer [Security]","_crypto2_cert_chain_policy_para","security.cert_chain_policy_para","wincrypt/CERT_CHAIN_POLICY_PARA","wincrypt/PCERT_CHAIN_POLICY_PARA"]
old-location: security\cert_chain_policy_para.htm
tech.root: security
ms.assetid: 5e4fffcb-132b-42c0-81b2-9f866e274c32
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_POLICY_PARA, BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_CA_FLAG, BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_END_ENTITY_FLAG, CERT_CHAIN_POLICY_ALLOW_TESTROOT_FLAG, CERT_CHAIN_POLICY_ALLOW_UNKNOWN_CA_FLAG, CERT_CHAIN_POLICY_IGNORE_ALL_NOT_TIME_VALID_FLAGS, CERT_CHAIN_POLICY_IGNORE_ALL_REV_UNKNOWN_FLAGS, CERT_CHAIN_POLICY_IGNORE_CA_REV_UNKNOWN_FLAG, CERT_CHAIN_POLICY_IGNORE_CTL_NOT_TIME_VALID_FLAG, CERT_CHAIN_POLICY_IGNORE_CTL_SIGNER_REV_UNKNOWN_FLAG, CERT_CHAIN_POLICY_IGNORE_END_REV_UNKNOWN_FLAG, CERT_CHAIN_POLICY_IGNORE_INVALID_BASIC_CONSTRAINTS_FLAG, CERT_CHAIN_POLICY_IGNORE_INVALID_NAME_FLAG, CERT_CHAIN_POLICY_IGNORE_INVALID_POLICY_FLAG, CERT_CHAIN_POLICY_IGNORE_NOT_SUPPORTED_CRITICAL_EXT_FLAG, CERT_CHAIN_POLICY_IGNORE_NOT_TIME_NESTED_FLAG, CERT_CHAIN_POLICY_IGNORE_NOT_TIME_VALID_FLAG, CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG, CERT_CHAIN_POLICY_IGNORE_ROOT_REV_UNKNOWN_FLAG, CERT_CHAIN_POLICY_IGNORE_WRONG_USAGE_FLAG, CERT_CHAIN_POLICY_PARA, CERT_CHAIN_POLICY_PARA structure [Security], CERT_CHAIN_POLICY_TRUST_TESTROOT_FLAG, MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG, PCERT_CHAIN_POLICY_PARA, PCERT_CHAIN_POLICY_PARA structure pointer [Security], _crypto2_cert_chain_policy_para, security.cert_chain_policy_para, wincrypt/CERT_CHAIN_POLICY_PARA, wincrypt/PCERT_CHAIN_POLICY_PARA'
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
req.typenames: CERT_CHAIN_POLICY_PARA, *PCERT_CHAIN_POLICY_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_POLICY_PARA
 - wincrypt/_CERT_CHAIN_POLICY_PARA
 - PCERT_CHAIN_POLICY_PARA
 - wincrypt/PCERT_CHAIN_POLICY_PARA
 - CERT_CHAIN_POLICY_PARA
 - wincrypt/CERT_CHAIN_POLICY_PARA
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
 - CERT_CHAIN_POLICY_PARA
---

# CERT_CHAIN_POLICY_PARA structure


## -description

The <b>CERT_CHAIN_POLICY_PARA</b> structure contains information used in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> to establish policy criteria for the verification of certificate chains.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwFlags

A set of flags that indicate conditions that could potentially be not valid and that are to be ignored in building certificate chains.


The <i>pszPolicyOID</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function can contain one of the following values:

<ul>
<li><b>CERT_CHAIN_POLICY_BASE</b></li>
<li><b>CERT_CHAIN_POLICY_AUTHENTICODE</b></li>
<li><b>CERT_CHAIN_POLICY_AUTHENTICODE_TS</b></li>
<li><b>CERT_CHAIN_POLICY_SSL</b></li>
<li><b>CERT_CHAIN_POLICY_NT_AUTH</b></li>
</ul>
If the <i>pszPolicyOID</i> parameter of the <b>CertVerifyCertificateChainPolicy</b> function contains one of the preceding values, then this member can be zero or a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_NOT_TIME_VALID_FLAG"></a><a id="cert_chain_policy_ignore_not_time_valid_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_NOT_TIME_VALID_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore not time valid errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_CTL_NOT_TIME_VALID_FLAG"></a><a id="cert_chain_policy_ignore_ctl_not_time_valid_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_CTL_NOT_TIME_VALID_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) not time valid errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_NOT_TIME_NESTED_FLAG"></a><a id="cert_chain_policy_ignore_not_time_nested_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_NOT_TIME_NESTED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore time nesting errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_ALL_NOT_TIME_VALID_FLAGS"></a><a id="cert_chain_policy_ignore_all_not_time_valid_flags"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_ALL_NOT_TIME_VALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Ignore all time validity errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_INVALID_BASIC_CONSTRAINTS_FLAG"></a><a id="cert_chain_policy_ignore_invalid_basic_constraints_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_INVALID_BASIC_CONSTRAINTS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore basic constraint errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_ALLOW_UNKNOWN_CA_FLAG"></a><a id="cert_chain_policy_allow_unknown_ca_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_ALLOW_UNKNOWN_CA_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Allow untrusted roots.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_WRONG_USAGE_FLAG"></a><a id="cert_chain_policy_ignore_wrong_usage_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_WRONG_USAGE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore invalid usage errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_INVALID_NAME_FLAG"></a><a id="cert_chain_policy_ignore_invalid_name_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_INVALID_NAME_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore invalid name errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_INVALID_POLICY_FLAG"></a><a id="cert_chain_policy_ignore_invalid_policy_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_INVALID_POLICY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore invalid policy errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_END_REV_UNKNOWN_FLAG"></a><a id="cert_chain_policy_ignore_end_rev_unknown_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_END_REV_UNKNOWN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignores errors in obtaining valid revocation information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_CTL_SIGNER_REV_UNKNOWN_FLAG"></a><a id="cert_chain_policy_ignore_ctl_signer_rev_unknown_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_CTL_SIGNER_REV_UNKNOWN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignores errors in obtaining  valid CTL revocation information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_CA_REV_UNKNOWN_FLAG"></a><a id="cert_chain_policy_ignore_ca_rev_unknown_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_CA_REV_UNKNOWN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignores errors in obtaining  valid <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) revocation information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_ROOT_REV_UNKNOWN_FLAG"></a><a id="cert_chain_policy_ignore_root_rev_unknown_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_ROOT_REV_UNKNOWN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignores errors in obtaining valid root revocation information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_ALL_REV_UNKNOWN_FLAGS"></a><a id="cert_chain_policy_ignore_all_rev_unknown_flags"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_ALL_REV_UNKNOWN_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Ignores errors in obtaining valid revocation information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_ALLOW_TESTROOT_FLAG"></a><a id="cert_chain_policy_allow_testroot_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_ALLOW_TESTROOT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Allow untrusted test roots.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_TRUST_TESTROOT_FLAG"></a><a id="cert_chain_policy_trust_testroot_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_TRUST_TESTROOT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Always trust test roots.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_NOT_SUPPORTED_CRITICAL_EXT_FLAG"></a><a id="cert_chain_policy_ignore_not_supported_critical_ext_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_NOT_SUPPORTED_CRITICAL_EXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore critical extension not supported errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG"></a><a id="cert_chain_policy_ignore_peer_trust_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore peer trusts.

</td>
</tr>
</table>
 


If the <i>pszPolicyOID</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function contains <b>CERT_CHAIN_POLICY_BASIC_CONSTRAINTS</b>, this member can be zero or a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG"></a><a id="cert_chain_policy_ignore_peer_trust_flag"></a><dl>
<dt><b>CERT_CHAIN_POLICY_IGNORE_PEER_TRUST_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore peer trusts.

</td>
</tr>
<tr>
<td width="40%"><a id="BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_CA_FLAG"></a><a id="basic_constraints_cert_chain_policy_ca_flag"></a><dl>
<dt><b>BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_CA_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Checks if the first certificate element is a CA.

</td>
</tr>
<tr>
<td width="40%"><a id="BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_END_ENTITY_FLAG"></a><a id="basic_constraints_cert_chain_policy_end_entity_flag"></a><dl>
<dt><b>BASIC_CONSTRAINTS_CERT_CHAIN_POLICY_END_ENTITY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Checks if the first certificate element is an end entity.

</td>
</tr>
</table>
 


If the <i>pszPolicyOID</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function contains <b>CERT_CHAIN_POLICY_MICROSOFT_ROOT</b>, this member can be zero or the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG"></a><a id="microsoft_root_cert_chain_policy_enable_test_root_flag"></a><dl>
<dt><b>MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Also check for the Microsoft test roots in addition to the Microsoft public root. 

<div class="alert"><b>Note</b>  The Windows test root certificate must be installed in the Trusted Root Certification Authorities certificate store for this to succeed.</div>
<div> </div>
</td>
</tr>
</table>

### -field pvExtraPolicyPara

The address of a pszPolicyOID-specific structure that provides additional validity policy conditions.