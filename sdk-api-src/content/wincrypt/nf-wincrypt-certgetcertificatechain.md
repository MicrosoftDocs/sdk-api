---
UID: NF:wincrypt.CertGetCertificateChain
title: CertGetCertificateChain function (wincrypt.h)
description: Builds a certificate chain context starting from an end certificate and going back, if possible, to a trusted root certificate.
helpviewer_keywords: ["CERT_CHAIN_CACHE_END_CERT","CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL","CERT_CHAIN_DISABLE_AIA","CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE","CERT_CHAIN_DISABLE_MY_PEER_TRUST","CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING","CERT_CHAIN_ENABLE_PEER_TRUST","CERT_CHAIN_OPT_IN_WEAK_SIGNATURE","CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS","CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT","CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY","CERT_CHAIN_REVOCATION_CHECK_CHAIN","CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT","CERT_CHAIN_REVOCATION_CHECK_END_CERT","CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT","CERT_CHAIN_TIMESTAMP_TIME","CertGetCertificateChain","CertGetCertificateChain function [Security]","_crypto2_certgetcertificatechain","security.certgetcertificatechain","wincrypt/CertGetCertificateChain"]
old-location: security\certgetcertificatechain.htm
tech.root: security
ms.assetid: 8c93036c-0b93-40d4-b0e3-ba1f2fc72db1
ms.date: 07/19/2024
ms.keywords: CERT_CHAIN_CACHE_END_CERT, CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL, CERT_CHAIN_DISABLE_AIA, CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE, CERT_CHAIN_DISABLE_MY_PEER_TRUST, CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING, CERT_CHAIN_ENABLE_PEER_TRUST, CERT_CHAIN_OPT_IN_WEAK_SIGNATURE, CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS, CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT, CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY, CERT_CHAIN_REVOCATION_CHECK_CHAIN, CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, CERT_CHAIN_REVOCATION_CHECK_END_CERT, CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT, CERT_CHAIN_TIMESTAMP_TIME, CertGetCertificateChain, CertGetCertificateChain function [Security], _crypto2_certgetcertificatechain, security.certgetcertificatechain, wincrypt/CertGetCertificateChain
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
 - CertGetCertificateChain
 - wincrypt/CertGetCertificateChain
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
 - CertGetCertificateChain
---

# CertGetCertificateChain function

## -description

The **CertGetCertificateChain** function builds a certificate chain context starting from an end certificate and going back, if possible, to a trusted [root certificate](/windows/win32/SecGloss/r-gly).

## -parameters

### -param hChainEngine [in, optional]

A handle of the chain engine (namespace and cache) to be used. If *hChainEngine* is `NULL`, the default chain engine, `HCCE_CURRENT_USER`, is used. This parameter can be set to `HCCE_LOCAL_MACHINE`.

### -param pCertContext [in]

A pointer to the [CERT_CONTEXT](ns-wincrypt-cert_context.md) of the end certificate, the certificate for which a chain is being built. This certificate context will be the zero-index element in the first simple chain.

### -param pTime [in, optional]

A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) variable that indicates the time for which the chain is to be validated. Note that the time does not affect trust list, revocation, or root store checking. The current system time is used if <b>NULL</b> is passed to this parameter. Trust in a particular certificate being a trusted root is based on the current [state](/windows/win32/SecGloss/s-gly) of the root store and not the state of the root store at a time passed in by this parameter. For revocation, a [certificate revocation list](/windows/win32/SecGloss/c-gly) (CRL), itself, must be valid at the current time. The value of this parameter is used to determine whether a certificate listed in a CRL has been revoked.

### -param hAdditionalStore [in]

A handle to any additional store to search for supporting certificates and [certificate trust lists](/windows/win32/SecGloss/c-gly) (CTLs). This parameter can be `NULL` if no additional store is to be searched.

### -param pChainPara [in]

A pointer to a [CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md) structure that includes chain-building parameters.

### -param dwFlags [in]

Flag values that indicate special processing. This parameter can be a combination of one or more of the  following flags.

| Value | Meaning |
|-------|---------|
| **CERT_CHAIN_CACHE_END_CERT**<br/>`0x00000001` | When this flag is set, the end certificate is cached, which might speed up the chain-building process. By default, the end certificate is not cached, and it would need to be verified each time a chain is built for it. |
| **CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY**<br/>`0x80000000` | Revocation checking only accesses cached URLs. This would prevent network retrieval of CRLs or OCSP for the end or CA certificates. **CACHE_ONLY** depends on a buddy on the machine to have already retrieved the CRL or OCSP from the network. |
| **CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT**<br/>`0x04000000` | This flag is used internally during chain building for an [online certificate status protocol](/windows/win32/SecGloss/o-gly) (OCSP) signer certificate to prevent cyclic revocation checks. During chain building, if the OCSP response is signed by an independent OCSP signer, then, in addition to the original chain build, there is a second chain built for the OCSP signer certificate itself. This flag is used during this second chain build to inhibit a recursive independent OCSP signer certificate. If the signer certificate contains the **szOID_PKIX_OCSP_NOCHECK** extension, revocation checking is skipped for the leaf signer certificate. Both OCSP and CRL checking are allowed.<br/><br/>**Windows Server 2003 and Windows XP:** This value is not supported. |
| **CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL**<br/>`0x00000004` | Uses only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects, such as CTL cabs, Third Party roots, and AIA issuers. Most roots should be in a crypt32.dll resource. If not, then this retrieval is necessary to prevent a chain building error. These cabs and roots are hosted on high performance Microsoft CDN servers.<br/><br/>**Note:** This flag is not applicable to revocation checking. Set **CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY** to use only cached URLs for revocation checking. Normally, CTL cabs are already pre-fetched via cryptsvc service. |
| **CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING**`0x00000040` | For performance reasons, the second pass of chain building only considers potential chain paths that have quality greater than or equal to the highest quality determined during the first pass. The first pass only considers valid signature, complete chain, and trusted roots to calculate chain quality. This flag can be set to disable this optimization and consider all potential chain paths during the second pass. |
| **CERT_CHAIN_DISABLE_MY_PEER_TRUST**<br/>`0x00000800` | This flag is not supported. Certificates in the "My" store are never considered for peer trust. |
| **CERT_CHAIN_ENABLE_PEER_TRUST**<br/>`0x00000400` | End entity certificates in the "TrustedPeople" store are trusted without performing any chain building. This function does not set the **CERT_TRUST_IS_PARTIAL_CHAIN** or **CERT_TRUST_IS_UNTRUSTED_ROOT** **dwErrorStatus** member bits of the  *ppChainContext* parameter.<br/><br/>**Windows Server 2003 and Windows XP:** This flag is not supported. |
| **CERT_CHAIN_OPT_IN_WEAK_SIGNATURE**<br/>`0x00010000` | Setting this flag indicates the caller wishes to opt into weak signature checks.<br/><br/>This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2. |
| **CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS**<br/>`0x00000080` | The default is to return only the highest quality chain path. Setting this flag will return the lower quality chains. These are returned in the **cLowerQualityChainContext** and **rgpLowerQualityChainContext** fields of the chain context. |
| **CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE**<br/>`0x00000100` | Setting this flag inhibits the auto update of third-party roots from the Windows Update Web Server. |
| **CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT**<br/>`0x08000000` | When you set **CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT** and you also specify a value for the *dwUrlRetrievalTimeout* member of the [CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md) structure, the value you specify in *dwUrlRetrievalTimeout* represents the cumulative timeout across all revocation URL retrievals.<br/><br/>If you set **CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT** but do not specify a *dwUrlRetrievalTimeout* value, the maximum cumulative timeout is set, by default, to 20 seconds. Each URL tested will timeout after half of the remaining cumulative balance has passed. That is, the first URL times out after 10 seconds, the second after 5 seconds, the third after 2.5 seconds and so on until a URL succeeds, 20 seconds has passed, or there are no more URLs to test.<br/><br/>If you do not set **CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT**, each revocation URL in the chain is assigned a maximum timeout equal to the value specified in *dwUrlRetrievalTimeout*. If you do not specify a value for the *dwUrlRetrievalTimeout* member, each revocation URL is assigned a maximum default timeout of 15 seconds.  If no URL succeeds, the maximum cumulative timeout value is 15 seconds multiplied by the number of URLs in the chain.<br/><br/>You can set the default values by using Group Policy. |
| **CERT_CHAIN_TIMESTAMP_TIME**<br/>`0x00000200` | When this flag is set, *pTime* is used as the time stamp time to determine whether the end certificate was time valid. Current time can also be used to determine whether the end certificate remains time valid. All other [certification authority](/windows/win32/SecGloss/c-gly) (CA) and root certificates in the chain are checked by using current time and not *pTime*. |
| **CERT_CHAIN_DISABLE_AIA**<br/>`0x00002000` | Setting this flag explicitly turns off Authority Information Access (AIA) retrievals. Sometimes TLS servers are incorrectly configured and don't include the correct CA certificates in the handshake. |

You can also set the following revocation flags, but only one flag from this group may be set at a time.

| Value | Meaning |
|-------|---------|
| **CERT_CHAIN_REVOCATION_CHECK_END_CERT**<br/>`0x10000000` | Revocation checking is done on the end certificate and only the end certificate. |
| **CERT_CHAIN_REVOCATION_CHECK_CHAIN**<br/>`0x20000000` | Revocation checking is done on all of the certificates in every chain. |
| **CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT**<br/>`0x40000000` | Revocation checking is done on all certificates in all of the chains except the root certificate. |

### -param pvReserved [in]

This parameter is reserved and must be `NULL`.

### -param ppChainContext [out]

The address of a pointer to the chain context created. When you have finished using the chain context, release the chain by calling the [CertFreeCertificateChain](nf-wincrypt-certfreecertificatechain.md) function.

## -returns

If the function succeeds, the function returns nonzero (`TRUE`).

If the function fails, it returns zero (`FALSE`). For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

When an application requests a certificate chain, the structure returned is in the form of a [CERT_CHAIN_CONTEXT](ns-wincrypt-cert_chain_context.md). This context contains an array of [CERT_SIMPLE_CHAIN](ns-wincrypt-cert_simple_chain.md) structures where each simple chain goes from an end certificate to a self-signed certificate. The chain context connects simple chains through trust lists. Each simple chain contains the chain of certificates, summary trust information about the chain, and trust information about each certificate element in the chain.

The following remarks apply to strong signature checking:

- You can enable strong signature checking for this function by setting the **pStrongSignPara** member of the [CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md) structure that is pointed to by the *pChainPara* parameter.
- If a certificate without a strong signature is found in the chain, the **CERT_TRUST_HAS_WEAK_SIGNATURE** and **CERT_TRUST_IS_NOT_SIGNATURE_VALID** errors are set in the **dwErrorStatus** field of the [CERT_TRUST_STATUS](ns-wincrypt-cert_trust_status.md) structure. The *ppChainContext* parameter points to a [CERT_CHAIN_CONTEXT](ns-wincrypt-cert_chain_context.md) structure which, in turn, points to the **CERT_TRUST_STATUS** structure.
- If the chain is strong signed, the public key in the end certificate is checked to determine whether it  satisfies the minimum public key length requirements for a strong signature. If the condition is not satisfied, the **CERT_TRUST_HAS_WEAK_SIGNATURE** and **CERT_TRUST_IS_NOT_SIGNATURE_VALID** errors are set in the **dwErrorStatus** field of the [CERT_TRUST_STATUS](ns-wincrypt-cert_trust_status.md) structure. To disable checking the key length, set the **CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG** value in the **dwStrongSignFlags** member of the [CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md) structure pointed to by the *pChainPara* parameter.
- If the **CERT_STRONG_SIGN_ENABLE_CRL_CHECK** or **CERT_STRONG_SIGN_ENABLE_OCSP_CHECK** flags are set in the [CERT_STRONG_SIGN_SERIALIZED_INFO](ns-wincrypt-cert_strong_sign_serialized_info.md) structure and a CRL or OCSP response is found without a strong signature, the CRL or OCSP response will be treated as being offline. That is, the **CERT_TRUST_IS_OFFLINE_REVOCATION** and **CERT_TRUST_REVOCATION_STATUS_UNKNOWN** errors are set in the **dwErrorStatus** field of the [CERT_TRUST_STATUS](ns-wincrypt-cert_trust_status.md) structure. Also, the **dwRevocationResult** member of the [CERT_REVOCATION_INFO](ns-wincrypt-cert_revocation_info.md) structure is set to **NTE_BAD_ALGID**.

The following recommendations would apply to any Windows application calling these APIs to verify a TLS server auth certificate:

- Only enable revocation checking for the end certificate.
  - Set **CERT_CHAIN_REVOCATION_CHECK_END_CERT** flag.
  - Most CA certificates have CRL’s with a time validity of 1 to 6 months.
    - Since downloaded CRLs are cached, this validity is too long to have much value.
  - If there is a CA compromise, then the certificate(s) would also be added to the Windows Disallowed CTL
  - The recommended practice for TLS servers is to support OCSP stapling for end certificate.
    - In that case, no network retrievals will be necessary unless the stapled OCSP response has expired.
- Enable network retrievals for CRLs, OCSP, AIA issuers and Windows platform CTL cabs and Third Party roots.
  - When the above **CERT_CHAIN_REVOCATION_CHECK_END_CERT** is set, this is the default.
  - Don’t set any of the following flags to prevent network retrievals. See the *dwFlags* table above for more information about these flags:
    - **CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL**
    - **CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY**
    - **CERT_CHAIN_DISABLE_AIA**
- Enable accumulative timeout for CRL and OCSP network retrievals.
  - Set the **CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT** flag passed to **CertGetCertificateChain**.
  - Provides an upper limit on the total time allowed for CRL and OCSP network retrievals.
- Reduce the maximum time allowed for each network retrieval from 15 to 10 seconds.
  - Set the **dwUrlRetrievalTimeout** field in the **CERT_CHAIN_PARA** passed to **CertGetCertificateChain** to 10 * 1000 milliseconds.
  - This also reduces the accumulative timeout from 20 to 10 seconds.
    - Only OCSP responses should be downloaded for end certificates. 5 seconds should be sufficient for that download.
- Ignore offline revocation errors.
  - Set **CERT_CHAIN_POLICY_IGNORE_ALL_REV_UNKNOWN_FLAGS** in the **CERT_CHAIN_POLICY_PARA** passed to [CertVerifyCertificateChainPolicy(CERT_CHAIN_POLICY_SSL)](nf-wincrypt-certverifycertificatechainpolicy.md).
  - The network retrieval of OCSP and CRL is best attempt. Most network retrievals should succeed under a couple of seconds, but it isn't 100% guaranteed.
- Cache end certificate validation information.
  - Set the **CERT_CHAIN_CACHE_END_CERT**.
    - Enables LRU caching of information on end certificates in addition to intermediate certificates.
  - It is common to make multiple TLS connections to the same server.

#### Examples

For an example that uses this function, see [Example C Program: Creating a Certificate Chain](/windows/win32/SecCrypto/example-c-program-creating-a-certificate-chain).

## -see-also

[CERT_CHAIN_PARA](ns-wincrypt-cert_chain_para.md)

[CertDuplicateCertificateChain](nf-wincrypt-certduplicatecertificatechain.md)

[CertFreeCertificateChain](nf-wincrypt-certfreecertificatechain.md)

[Certificate Chain Verification Functions](/windows/win32/SecCrypto/cryptography-functions)
