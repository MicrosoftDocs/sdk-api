---
UID: NF:wincrypt.CertVerifyCertificateChainPolicy
title: CertVerifyCertificateChainPolicy function (wincrypt.h)
description: Checks a certificate chain to verify its validity, including its compliance with any specified validity policy criteria.
helpviewer_keywords: ["CERT_CHAIN_POLICY_AUTHENTICODE","CERT_CHAIN_POLICY_AUTHENTICODE_TS","CERT_CHAIN_POLICY_BASE","CERT_CHAIN_POLICY_BASIC_CONSTRAINTS","CERT_CHAIN_POLICY_EV","CERT_CHAIN_POLICY_MICROSOFT_ROOT","CERT_CHAIN_POLICY_NT_AUTH","CERT_CHAIN_POLICY_SSL","CERT_CHAIN_POLICY_SSL_F12","CertVerifyCertificateChainPolicy","CertVerifyCertificateChainPolicy function [Security]","_crypto2_certverifycertificatechainpolicy","security.certverifycertificatechainpolicy","wincrypt/CertVerifyCertificateChainPolicy"]
old-location: security\certverifycertificatechainpolicy.htm
tech.root: security
ms.assetid: 19c37f77-1072-4740-b244-764b816a2a1f
ms.date: 07/19/2024
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

The **CertVerifyCertificateChainPolicy** function checks a certificate chain to verify its validity, including its compliance with any specified validity policy criteria.

## -parameters

### -param pszPolicyOID [in]

Current predefined verify chain policy structures are listed in the following table.

| Value | Meaning |
|-------|---------|
| **CERT_CHAIN_POLICY_BASE**<br/>(LPCSTR) 1 | Implements the base chain policy verification checks. The **dwFlags** member of the structure pointed to by *pPolicyPara* can be set to alter the default policy checking behavior. |
| **CERT_CHAIN_POLICY_AUTHENTICODE**</br>(LPCSTR) 2 | Implements the Authenticode chain policy verification checks. The **pvExtraPolicyPara** member of the structure pointed to by *pPolicyPara* can be set to point to an [AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA](ns-wincrypt-authenticode_extra_cert_chain_policy_para.md) structure.<br/><br/>The **pvExtraPolicyStatus** member of the structure pointed to by *pPolicyStatus* can be set to point to an [AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS](ns-wincrypt-authenticode_extra_cert_chain_policy_status.md) structure. |
| **CERT_CHAIN_POLICY_AUTHENTICODE_TS**<br/>(LPCSTR) 3 | Implements Authenticode Time Stamp chain policy verification checks. The **pvExtraPolicyPara** member of the data structure pointed to by *pPolicyPara* can be set to point to an [AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA](ns-wincrypt-authenticode_ts_extra_cert_chain_policy_para.md) structure.<br/><br/>The **pvExtraPolicyStatus** member of the data structure pointed to by *pPolicyStatus* is not used and must be set to `NULL`. |
| **CERT_CHAIN_POLICY_SSL**<br/>(LPCSTR) 4 | Implements the SSL client/server chain policy verification checks. The **pvExtraPolicyPara** member in the data structure pointed to by *pPolicyPara* can be set to point to an [SSL_EXTRA_CERT_CHAIN_POLICY_PARA](ns-wincrypt-httpspolicycallbackdata.md) structure initialized with additional policy criteria.<br/><br/>**Note:** To differentiate between server and client authorization certificates, the call to the [CertGetCertificateChain](nf-wincrypt-certgetcertificatechain.md) function to get the chain context should specify the  certificate type by setting the expected usage. Set the expected usage by setting the **RequestedUsage** member of the [CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md) structure passed in the *pChainPara* input parameter of the **CertGetCertificateChain** function. |
| **CERT_CHAIN_POLICY_BASIC_CONSTRAINTS**<br/>(LPCSTR) 5 | Implements the basic constraints chain policy. Iterates through all the certificates in the chain checking for either a **szOID_BASIC_CONSTRAINTS** or a **szOID_BASIC_CONSTRAINTS2** extension. If neither extension is present, the certificate is assumed to have valid policy. Otherwise, for the first certificate element, checks if it matches the expected CA_FLAG or END_ENTITY_FLAG specified in the **dwFlags** member of the [CERT_CHAIN_POLICY_PARA](ns-wincrypt-cert_chain_policy_para.md) structure pointed to by the *pPolicyPara* parameter. If neither or both flags are set, then, the first element can be either a CA or END_ENTITY. All other elements must be a [certification authority](/windows/win32/SecGloss/c-gly) (CA). If the PathLenConstraint is present in the extension, it is checked.<br/><br/>The first elements in the remaining simple chains (that is, the certificates used to sign the CTL) are checked to be an END_ENTITY. If this verification fails, **dwError** will be set to TRUST_E_BASIC_CONSTRAINTS. |
| **CERT_CHAIN_POLICY_NT_AUTH**<br/>(LPCSTR) 6 | Implements the Windows NT Authentication chain policy, which consists of three distinct chain verifications in the following order: <br/><br/>- CERT_CHAIN_POLICY_BASE: Implements the base chain policy verification checks. The LOWORD of <i>dwFlags</i> can be set in *pPolicyPara* to alter the default policy checking behavior. For more information, see CERT_CHAIN_POLICY_BASE.<br/>- CERT_CHAIN_POLICY_BASIC_CONSTRAINTS: Implements the basic constraints chain policy. The HIWORD of *dwFlags* can be set to specify if the first element must be either a CA or END_ENTITY. For more information, see CERT_CHAIN_POLICY_BASIC_CONSTRAINTS.<br/>- Checks if the second element in the chain, the CA that issued the end certificate, is a trusted CA for Windows NT Authentication. A CA is considered to be trusted if it exists in the "NTAuth" system registry store found in the CERT_SYSTEM_STORE_LOCAL_MACHINE_ENTERPRISE store location. If this verification fails, the CA is untrusted, and *dwError* is set to CERT_E_UNTRUSTEDCA. If CERT_PROT_ROOT_DISABLE_NT_AUTH_REQUIRED_FLAG is set in the **Flags** value of the **HKEY_LOCAL_MACHINE** policy **ProtectedRoots** subkey, defined by CERT_PROT_ROOT_FLAGS_REGPATH and the above check fails, the chain is checked for CERT_TRUST_HAS_VALID_NAME_CONSTRAINTS set in *dwInfoStatus*. This is set if there was a valid name constraint for all namespaces including UPN. If the chain does not have this info status set, *dwError* is set to CERT_E_UNTRUSTEDCA. |
| **CERT_CHAIN_POLICY_MICROSOFT_ROOT**<br/>(LPCSTR) 7 | Checks the last element of the first simple chain for a Microsoft root public key. If that element does not contain a Microsoft root public key, the **dwError** member of the [CERT_CHAIN_POLICY_STATUS](ns-wincrypt-cert_chain_policy_status.md) structure pointed to by the *pPolicyStatus* parameter is set to **CERT_E_UNTRUSTEDROOT**.<br/><br/>The **dwFlags** member of the [CERT_CHAIN_POLICY_PARA](ns-wincrypt-cert_chain_policy_para.md) structure pointed to by the *pPolicyStatus* parameter can contain the **MICROSOFT_ROOT_CERT_CHAIN_POLICY_CHECK_APPLICATION_ROOT_FLAG** flag, which causes this function to instead check for the Microsoft application root "Microsoft Root Certificate Authority 2011".<br/><br/>The **dwFlags** member of the [CERT_CHAIN_POLICY_PARA](ns-wincrypt-cert_chain_policy_para.md) structure pointed to by the *pPolicyPara* parameter can contain the **MICROSOFT_ROOT_CERT_CHAIN_POLICY_ENABLE_TEST_ROOT_FLAG** flag, which causes this function to also check for the Microsoft test roots.<br/><br/>**Note:**<br/>This policy [object identifier](/windows/win32/SecGloss/o-gly) (OID) does not perform any policy verification checks by itself, it is meant to be used in conjunction with other policies. |
| **CERT_CHAIN_POLICY_EV**<br/>(LPCSTR) 8 | Specifies that extended validation of certificates is performed.<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported. |
| **CERT_CHAIN_POLICY_SSL_F12**<br/>(LPCSTR) 9 | Checks if any certificates in the chain have weak crypto or if third party root certificate compliance and provide an error string. The **pvExtraPolicyStatus** member of the CERT_CHAIN_POLICY_STATUS structure pointed to by the *pPolicyStatus* parameter must point to [SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS](ns-wincrypt-ssl_f12_extra_cert_chain_policy_status.md), which is updated with the results of the weak crypto and root program compliance checks.<br/><br/>Before calling, the **cbSize** member of the CERT_CHAIN_POLICY_STATUS structure pointed to by the *pPolicyStatus* parameter must be set to a value greater than or equal to sizeof(SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS).<br/><br/>The **dwError** member in CERT_CHAIN_POLICY_STATUS structure pointed to by the *pPolicyStatus* parameter will be set to **TRUST_E_CERT_SIGNATURE** for potential weak crypto and set to **CERT_E_UNTRUSTEDROOT** for Third Party Roots not in compliance with the Microsoft Root Program.<br/><br/>**Windows 10, version 1607, Windows Server 2016, Windows 10, version 1511 with KB3172985, Windows 10 RTM with KB3163912, Windows 8.1 and Windows Server 2012 R2 with KB3163912, and Windows 7 with SP1 and Windows Server 2008 R2 SP1 with KB3161029** |

### -param pChainContext [in]

A pointer to a [CERT_CHAIN_CONTEXT](ns-wincrypt-cert_chain_context.md) structure that contains a chain to be verified.

### -param pPolicyPara [in]

A pointer to a [CERT_CHAIN_POLICY_PARA](ns-wincrypt-cert_chain_policy_para.md) structure that provides the policy verification criteria for the chain. The **dwFlags** member of that structure can be set to change the default policy checking behavior.

In addition, policy-specific parameters can also be passed in the **pvExtraPolicyPara** member of the structure.

### -param pPolicyStatus [in, out]

A pointer to a [CERT_CHAIN_POLICY_STATUS](ns-wincrypt-cert_chain_policy_status.md) structure where status information on the chain is returned. OID-specific extra status can be returned in the **pvExtraPolicyStatus** member of this structure.

## -returns

The return value indicates whether the function was able to check for the policy, it does not indicate whether the policy check failed or passed.

If the chain can be verified for the specified policy, `TRUE` is returned and the **dwError** member of the *pPolicyStatus* is updated. A *dwError* of `0` (**ERROR_SUCCESS** or **S_OK**) indicates the chain satisfies the specified policy.

If the chain cannot be validated, the return value is `TRUE` and you need to verify the *pPolicyStatus* parameter for the actual error.

A value of `FALSE` indicates that the function wasn't able to check for the policy.

## -remarks

A **dwError** member of the [CERT_CHAIN_POLICY_STATUS](ns-wincrypt-cert_chain_policy_status.md) structure pointed to by *pPolicyStatus* can apply to a single chain element, to a simple chain, or to an entire chain context. If **dwError** applies to the entire chain context, both the **lChainIndex** and the **lElementIndex** members of the **CERT_CHAIN_POLICY_STATUS** structure are set to `–1`. If **dwError** applies to a complete simple chain, **lElementIndex** is set to `–1` and **lChainIndex** is set to the index of the first chain that has an error. If **dwError** applies to a single certificate element, **lChainIndex** and **lElementIndex** index the first certificate that has the error.

To get the certificate element use this syntax:

```
pChainContext->rgpChain[lChainIndex]->rgpElement[lElementIndex];
```

Use the [CertGetCertificateChain](nf-wincrypt-certgetcertificatechain.md) function to enable and perform certificate revocation checking.  The **CertVerifyCertificateChainPolicy** function does not check if certificates in the certificate chain are revoked.

## -see-also

[AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA](ns-wincrypt-authenticode_extra_cert_chain_policy_para.md)

[AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS](ns-wincrypt-authenticode_extra_cert_chain_policy_status.md)

[AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA](ns-wincrypt-authenticode_ts_extra_cert_chain_policy_para.md)

[CERT_CHAIN_CONTEXT](ns-wincrypt-cert_chain_context.md)

[CERT_CHAIN_POLICY_PARA](ns-wincrypt-cert_chain_policy_para.md)

[CERT_CHAIN_POLICY_STATUS](ns-wincrypt-cert_chain_policy_status.md)

[CertGetCertificateChain](nf-wincrypt-certgetcertificatechain.md)

[Certificate Chain Verification Functions](/windows/win32/SecCrypto/cryptography-functions)
