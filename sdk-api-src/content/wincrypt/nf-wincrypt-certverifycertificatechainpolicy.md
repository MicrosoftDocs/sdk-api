---
UID: NF:wincrypt.CertVerifyCertificateChainPolicy
title: CertVerifyCertificateChainPolicy function (wincrypt.h)
description: Checks a certificate chain to verify its validity, including its compliance with any specified validity policy criteria.
helpviewer_keywords: ["CERT_CHAIN_POLICY_AUTHENTICODE","CERT_CHAIN_POLICY_AUTHENTICODE_TS","CERT_CHAIN_POLICY_BASE","CERT_CHAIN_POLICY_BASIC_CONSTRAINTS","CERT_CHAIN_POLICY_EV","CERT_CHAIN_POLICY_MICROSOFT_ROOT","CERT_CHAIN_POLICY_NT_AUTH","CERT_CHAIN_POLICY_SSL","CERT_CHAIN_POLICY_SSL_F12","CertVerifyCertificateChainPolicy","CertVerifyCertificateChainPolicy function [Security]","_crypto2_certverifycertificatechainpolicy","security.certverifycertificatechainpolicy","wincrypt/CertVerifyCertificateChainPolicy"]
old-location: security\certverifycertificatechainpolicy.htm
tech.root: security
ms.assetid: 19c37f77-1072-4740-b244-764b816a2a1f
ms.date: 12/05/2018
ms.keywords: CERT_CHAIN_POLICY_AUTHENTICODE, CERT_CHAIN_POLICY_AUTHENTICODE_TS, CERT_CHAIN_POLICY_BASE, CERT_CHAIN_POLICY_BASIC_CONSTRAINTS, CERT_CHAIN_POLICY_EV, CERT_CHAIN_POLICY_MICROSOFT_ROOT, CERT_CHAIN_POLICY_NT_AUTH, CERT_CHAIN_POLICY_SSL, CERT_CHAIN_POLICY_SSL_F12, CertVerifyCertificateChainPolicy, CertVerifyCertificateChainPolicy function [Security], _crypto2_certverifycertificatechainpolicy, security.certverifycertificatechainpolicy, wincrypt/CertVerifyCertificateChainPolicy
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertVerifyCertificateChainPolicy
 - wincrypt/CertVerifyCertificateChainPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifyCertificateChainPolicy
---

# CertVerifyCertificateChainPolicy function


## -description

The <b>CertVerifyCertificateChainPolicy</b> function checks a certificate chain to verify its validity, including its compliance with any specified validity policy criteria.

## -parameters

### -param pszPolicyOID [in]

Current predefined verify chain policy structures are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_BASE"></a><a id="cert_chain_policy_base"></a><dl>
<dt><b>CERT_CHAIN_POLICY_BASE</b></dt>
<dt>(LPCSTR) 1</dt>
</dl>
</td>
<td width="60%">
Implements the base chain policy verification checks. The <b>dwFlags</b> member of the structure pointed to by <i>pPolicyPara</i> can be set to alter the default policy checking behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_AUTHENTICODE"></a><a id="cert_chain_policy_authenticode"></a><dl>
<dt><b>CERT_CHAIN_POLICY_AUTHENTICODE</b></dt>
<dt>(LPCSTR) 2</dt>
</dl>
</td>
<td width="60%">
Implements the Authenticode chain policy verification checks. The <b>pvExtraPolicyPara</b> member of the structure pointed to by <i>pPolicyPara</i> can be set to point to an 
<a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_extra_cert_chain_policy_para">AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA</a> structure.

The <b>pvExtraPolicyStatus</b> member of the structure pointed to by <i>pPolicyStatus</i> can be set to point to an <a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_extra_cert_chain_policy_status">AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_AUTHENTICODE_TS"></a><a id="cert_chain_policy_authenticode_ts"></a><dl>
<dt><b>CERT_CHAIN_POLICY_AUTHENTICODE_TS</b></dt>
<dt>(LPCSTR) 3</dt>
</dl>
</td>
<td width="60%">
Implements Authenticode Time Stamp chain policy verification checks. The <b>pvExtraPolicyPara</b> member of the data structure pointed to by <i>pPolicyPara</i> can be set to point to an <a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_ts_extra_cert_chain_policy_para">AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA</a> structure.

The <b>pvExtraPolicyStatus</b> member of the data structure pointed to by <i>pPolicyStatus</i> is not used and must be set to <b>NULL</b>

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL"></a><a id="cert_chain_policy_ssl"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL</b></dt>
<dt>(LPCSTR) 4</dt>
</dl>
</td>
<td width="60%">
Implements the SSL client/server chain policy verification checks. The <b>pvExtraPolicyPara</b> member in the data structure pointed to by <i>pPolicyPara</i> can be set to point to an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-httpspolicycallbackdata">SSL_EXTRA_CERT_CHAIN_POLICY_PARA</a> structure initialized with additional policy criteria.

<div class="alert"><b>Note</b>  To differentiate between server and client authorization certificates,  the call to the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function to get the chain context should specify the  certificate type by setting the expected usage. Set the expected usage by setting the <b>RequestedUsage</b> member of the  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure passed in the <i>pChainPara</i> input parameter of the <b>CertGetCertificateChain</b> function.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_BASIC_CONSTRAINTS"></a><a id="cert_chain_policy_basic_constraints"></a><dl>
<dt><b>CERT_CHAIN_POLICY_BASIC_CONSTRAINTS</b></dt>
<dt>(LPCSTR) 5</dt>
</dl>
</td>
<td width="60%">
Implements the basic constraints chain policy. Iterates through all the certificates in the chain checking for either a szOID_BASIC_CONSTRAINTS or a szOID_BASIC_CONSTRAINTS2 extension. If neither extension is present, the certificate is assumed to have valid policy. Otherwise, for the first certificate element, checks if it matches the expected CA_FLAG or END_ENTITY_FLAG specified in the <b>dwFlags</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para">CERT_CHAIN_POLICY_PARA</a> structure pointed to by the <i>pPolicyPara</i> parameter. If neither or both flags are set, then, the first element can be either a CA or END_ENTITY. All other elements must be a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). If the PathLenConstraint is present in the extension, it is checked.

The first elements in the remaining simple chains (that is, the certificates used to sign the CTL) are checked to be an END_ENTITY. If this verification fails, <b>dwError</b> will be set to TRUST_E_BASIC_CONSTRAINTS.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_NT_AUTH"></a><a id="cert_chain_policy_nt_auth"></a><dl>
<dt><b>CERT_CHAIN_POLICY_NT_AUTH</b></dt>
<dt>(LPCSTR) 6</dt>
</dl>
</td>
<td width="60%">
Implements the Windows NT Authentication chain policy, which consists of three distinct chain verifications in the following order: 




<ol>
<li>CERT_CHAIN_POLICY_BASE—Implements the base chain policy verification checks. The LOWORD of <i>dwFlags</i> can be set in <i>pPolicyPara</i> to alter the default policy checking behavior. For more information, see CERT_CHAIN_POLICY_BASE.</li>
<li>CERT_CHAIN_POLICY_BASIC_CONSTRAINTS—Implements the basic constraints chain policy. The HIWORD of <i>dwFlags</i> can be set to specify if the first element must be either a CA or END_ENTITY. For more information, see CERT_CHAIN_POLICY_BASIC_CONSTRAINTS.</li>
<li>Checks if the second element in the chain, the CA that issued the end certificate, is a trusted CA for Windows NT Authentication. A CA is considered to be trusted if it exists in the "NTAuth" system registry store found in the CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE store location. If this verification fails, the CA is untrusted, and <i>dwError</i> is set to CERT_E_UNTRUSTEDCA.If CERT_PROT_ROOT_DISABLE_NT_AUTH_REQUIRED_FLAG is set in the <b>Flags</b> value of the <b>HKEY_LOCAL_MACHINE</b> policy <b>ProtectedRoots</b> subkey, defined by CERT_PROT_ROOT_FLAGS_REGPATH and the above check fails, the chain is checked for CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS set in <i>dwInfoStatus</i>. This is set if there was a valid name constraint for all namespaces including UPN. If the chain does not have this info status set, <i>dwError</i> is set to CERT_E_UNTRUSTEDCA.

</li>
</ol>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_MICROSOFT_ROOT"></a><a id="cert_chain_policy_microsoft_root"></a><dl>
<dt><b>CERT_CHAIN_POLICY_MICROSOFT_ROOT</b></dt>
<dt>(LPCSTR) 7</dt>
</dl>
</td>
<td width="60%">
Checks the last element of the first simple chain for a Microsoft root public key. If that element does not contain a Microsoft root public key, the <b>dwError</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a> structure pointed to by the <i>pPolicyStatus</i> parameter is set to <b>CERT_E_UNTRUSTEDROOT</b>.

The <b>dwFlags</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para">CERT_CHAIN_POLICY_PARA</a> structure pointed to by the <i>pPolicyStatus</i> parameter can contain the <b>MICROSOFT_ROOT_CERT_CHAIN_POLICY_CHECK_APPLICATION_ROOT_FLAG</b> flag, which causes this function to instead check for the Microsoft application root "Microsoft Root Certificate Authority 2011".

The <b>dwFlags</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para">CERT_CHAIN_POLICY_PARA</a> structure pointed to by the <i>pPolicyPara</i> parameter can contain the <b>MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG</b> flag, which causes this function to also check for the Microsoft test roots.

<div class="alert"><b>Note</b>  This policy <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) does not perform any policy verification checks by itself, it is meant to be used in conjunction with other policies.
</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_EV"></a><a id="cert_chain_policy_ev"></a><dl>
<dt><b>CERT_CHAIN_POLICY_EV</b></dt>
<dt>(LPCSTR) 8</dt>
</dl>
</td>
<td width="60%">
Specifies that extended validation of certificates is performed.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12"></a><a id="cert_chain_policy_ssl_f12"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12</b></dt>
<dt>(LPCSTR) 9</dt>
</dl>
</td>
<td width="60%">
Checks if any certificates in the chain have weak crypto or if third party root certificate compliance and provide an error string. The <b>pvExtraPolicyStatus</b> member of the CERT_CHAIN_POLICY_STATUS structure pointed to by the <i>pPolicyStatus</i> parameter must point to <a href="/windows/win32/api/wincrypt/ns-wincrypt-ssl_f12_extra_cert_chain_policy_status">SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS</a>, which is updated with the results of the weak crypto and root program compliance checks.

Before calling, the <b>cbSize</b> member of the 	CERT_CHAIN_POLICY_STATUS structure pointed to by the <i>pPolicyStatus</i> parameter must be set to a value greater than or equal to sizeof(SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS).

The <b>dwError</b> member in CERT_CHAIN_POLICY_STATUS structure pointed to by the <i>pPolicyStatus</i> parameter will be set to <b>TRUST_E_CERT_SIGNATURE</b> for potential weak crypto and set to <b>CERT_E_UNTRUSTEDROOT</b> for Third Party Roots not in compliance with the Microsoft Root Program. 

<b>Windows 10, version 1607, Windows Server 2016, Windows 10, version 1511 with KB3172985, Windows 10 RTM with KB3163912, Windows 8.1 and Windows Server 2012 R2 with KB3163912, and Windows 7 with SP1 and Windows Server 2008 R2 SP1 with KB3161029</b>

</td>
</tr>
</table>

### -param pChainContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structure that contains a chain to be verified.

### -param pPolicyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para">CERT_CHAIN_POLICY_PARA</a> structure that provides the policy verification criteria for the chain. The <b>dwFlags</b> member of that structure can be set to change the default policy checking behavior. 




In addition, policy-specific parameters can also be passed in the <b>pvExtraPolicyPara</b> member of the structure.

### -param pPolicyStatus [in, out]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a> structure where status information on the chain is returned. OID-specific extra status can be returned in the <b>pvExtraPolicyStatus</b> member of this structure.

## -returns

The return value indicates whether the function was able to check for the policy, it does not indicate whether the policy check failed or passed. 

If the chain can be verified for the specified policy, <b>TRUE</b> is returned and the <b>dwError</b> member of the <i>pPolicyStatus</i> is updated. A <b>dwError</b> of 0 (ERROR_SUCCESS or S_OK) indicates the chain satisfies the specified policy.

If the chain cannot be validated, the return value is  <b>TRUE</b> and you need to verify the <i>pPolicyStatus</i> parameter for the actual error.

A value of <b>FALSE</b>  indicates that the function wasn't able to check for the policy.

## -remarks

A <b>dwError</b> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a> structure pointed to by <i>pPolicyStatus</i> can apply to a single chain element, to a simple chain, or to an entire chain context. If <b>dwError</b> applies to the entire chain context, both the <b>lChainIndex</b> and the <b>lElementIndex</b> members of the <b>CERT_CHAIN_POLICY_STATUS</b> structure are set to –1. If <b>dwError</b> applies to a complete simple chain, <b>lElementIndex</b> is set to –1 and <b>lChainIndex</b> is set to the index of the first chain that has an error. If <b>dwError</b> applies to a single certificate element, <b>lChainIndex</b> and <b>lElementIndex</b> index the first certificate that has the error. 

To get the certificate element use this syntax: 

<code>pChainContext-&gt;rgpChain[lChainIndex]-&gt;rgpElement[lElementIndex];</code>

Use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function to enable and perform certificate revocation checking.  The <b>CertVerifyCertificateChainPolicy</b> function does not check if certificates in the certificate chain are revoked.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_extra_cert_chain_policy_para">AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA</a>



<a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_extra_cert_chain_policy_status">AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS</a>



<a href="/windows/win32/api/wincrypt/ns-wincrypt-authenticode_ts_extra_cert_chain_policy_para">AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para">CERT_CHAIN_POLICY_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a>