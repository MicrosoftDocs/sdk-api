---
UID: NF:wincrypt.CertGetCertificateChain
title: CertGetCertificateChain function
author: windows-driver-content
description: Builds a certificate chain context starting from an end certificate and going back, if possible, to a trusted root certificate.
old-location: security\certgetcertificatechain.htm
old-project: SecCrypto
ms.assetid: 8c93036c-0b93-40d4-b0e3-ba1f2fc72db1
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CERT_CHAIN_CACHE_END_CERT, CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL, CERT_CHAIN_DISABLE_AIA, CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE, CERT_CHAIN_DISABLE_MY_PEER_TRUST, CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING, CERT_CHAIN_ENABLE_PEER_TRUST, CERT_CHAIN_OPT_IN_WEAK_SIGNATURE, CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS, CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT, CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY, CERT_CHAIN_REVOCATION_CHECK_CHAIN, CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, CERT_CHAIN_REVOCATION_CHECK_END_CERT, CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT, CERT_CHAIN_TIMESTAMP_TIME, CertGetCertificateChain, CertGetCertificateChain function [Security], _crypto2_certgetcertificatechain, security.certgetcertificatechain, wincrypt/CertGetCertificateChain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertGetCertificateChain
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertGetCertificateChain function


## -description



			The <b>CertGetCertificateChain</b> function builds a certificate chain context starting from an end certificate and going back, if possible, to a trusted <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">root certificate</a>.


## -parameters




### -param hChainEngine [in, optional]

A handle of the chain engine (namespace and cache) to be used. If <i>hChainEngine</i> is <b>NULL</b>, the default chain engine, HCCE_CURRENT_USER, is used. This parameter can be set to HCCE_LOCAL_MACHINE.


### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the end certificate, the certificate for which a chain is being built. This certificate context will be the zero-index element in the first simple chain.


### -param pTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> variable that indicates the time for which the chain is to be validated. Note that the time does not affect trust list, revocation, or root store checking. The current system time is used if <b>NULL</b> is passed to this parameter. Trust in a particular certificate being a trusted root is based on the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the root store and not the state of the root store at a time passed in by this parameter. For revocation, a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL), itself, must be valid at the current time. The value of this parameter is used to determine whether a certificate listed in a CRL has been revoked.


### -param hAdditionalStore [in]

A handle to any additional store to search for supporting certificates and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> (CTLs). This parameter can be <b>NULL</b> if no additional store is to be searched. 


### -param pChainPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure that includes chain-building parameters.


### -param dwFlags [in]

Flag values that indicate special processing. This parameter can be a combination of one or more of the  following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_END_CERT"></a><a id="cert_chain_cache_end_cert"></a><dl>
<dt><b>CERT_CHAIN_CACHE_END_CERT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
When this flag is set, the end certificate is cached, which might speed up the chain-building process. By default, the end certificate is not cached, and it would need to be verified each time a chain is built for it.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY"></a><a id="cert_chain_revocation_check_cache_only"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Revocation checking only accesses cached URLs.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT"></a><a id="cert_chain_revocation_check_ocsp_cert"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
This flag is used internally during chain building for an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) signer certificate to prevent cyclic revocation checks. During chain building, if the OCSP response is signed by an independent OCSP signer, then, in addition to the original chain build, there is a second chain built for the OCSP signer certificate itself. This flag is used during this second chain build to inhibit a recursive independent OCSP signer certificate. If the signer certificate contains the
<b>szOID_PKIX_OCSP_NOCHECK</b> extension, revocation checking is skipped
for the leaf signer certificate. Both OCSP and CRL checking are allowed.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL"></a><a id="cert_chain_cache_only_url_retrieval"></a><dl>
<dt><b>CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Uses only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects. 

<b>Note</b>  This flag is not applicable to revocation checking. Set CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY to use only cached URLs for revocation checking.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING"></a><a id="cert_chain_disable_pass1_quality_filtering"></a><dl>
<dt><b>CERT_CHAIN_DISABLE_PASS1_QUALITY_FILTERING</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
For performance reasons, the second pass of chain building only considers potential chain paths that have quality greater than or equal to the highest quality determined during the first pass. The first pass only considers valid signature, complete chain, and trusted roots to calculate chain quality. This flag can be set to disable this optimization and consider all potential chain paths during the second pass.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_DISABLE_MY_PEER_TRUST"></a><a id="cert_chain_disable_my_peer_trust"></a><dl>
<dt><b>CERT_CHAIN_DISABLE_MY_PEER_TRUST</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
This flag is not supported. Certificates in the "My" store are never considered for peer trust.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_ENABLE_PEER_TRUST"></a><a id="cert_chain_enable_peer_trust"></a><dl>
<dt><b>CERT_CHAIN_ENABLE_PEER_TRUST</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
End entity certificates in the "TrustedPeople" store are trusted without performing any chain building. This function does not set the <b>CERT_TRUST_IS_PARTIAL_CHAIN</b> or <b>CERT_TRUST_IS_UNTRUSTED_ROOT</b> <b>dwErrorStatus</b> member bits of the  <i>ppChainContext</i> parameter.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_OPT_IN_WEAK_SIGNATURE"></a><a id="cert_chain_opt_in_weak_signature"></a><dl>
<dt><b>CERT_CHAIN_OPT_IN_WEAK_SIGNATURE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Setting this flag indicates the caller wishes to opt into weak signature checks.

This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS"></a><a id="cert_chain_return_lower_quality_contexts"></a><dl>
<dt><b>CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The default is to return only the highest quality chain path. Setting this flag will return the lower quality chains. These are returned in the <b>cLowerQualityChainContext</b> and <b>rgpLowerQualityChainContext</b> fields of the chain context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE"></a><a id="cert_chain_disable_auth_root_auto_update"></a><dl>
<dt><b>CERT_CHAIN_DISABLE_AUTH_ROOT_AUTO_UPDATE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Setting this flag inhibits the auto update of third-party roots from the Windows Update Web Server.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT"></a><a id="cert_chain_revocation_accumulative_timeout"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
When you set CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT and you also specify a value for the <i>dwUrlRetrievalTimeout</i> member of the <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure, the value you specify in <i>dwUrlRetrievalTimeout</i> represents the cumulative timeout across all revocation URL retrievals.

If you set CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT but do not specify a <i>dwUrlRetrievalTimeout</i> value, the maximum cumulative timeout is set, by default, to 20 seconds. Each URL tested will timeout after half of the remaining cumulative balance has passed. That is, the first URL times out after 10 seconds, the second after 5 seconds, the third after 2.5 seconds and so on until a URL succeeds, 20 seconds has passed, or there are no more URLs to test.

If you do not set CERT_CHAIN_REVOCATION_ACCUMULATIVE_TIMEOUT, each revocation URL in the chain is assigned a maximum timeout equal to the value specified in <i>dwUrlRetrievalTimeout</i>. If you do not specify a value for the <i>dwUrlRetrievalTimeout</i> member, each revocation URL is assigned a maximum default timeout of 15 seconds.  If no URL succeeds, the maximum cumulative timeout value is 15 seconds multiplied by the number of URLs in the chain.

You can set the default values by using Group Policy.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_TIMESTAMP_TIME"></a><a id="cert_chain_timestamp_time"></a><dl>
<dt><b>CERT_CHAIN_TIMESTAMP_TIME</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
When this flag is set, <i>pTime</i> is used as the time stamp time to determine whether the end certificate was time valid. Current time can also be used to determine whether the end certificate remains time valid. All other <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) and root certificates in the chain are checked by using current time and not <i>pTime</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_DISABLE_AIA"></a><a id="cert_chain_disable_aia"></a><dl>
<dt><b>CERT_CHAIN_DISABLE_AIA</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Setting this flag explicitly turns off  Authority Information Access (AIA) retrievals.

</td>
</tr>
</table>
 

You can also set the following revocation flags, but only one flag from this group may be set at a time.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_END_CERT"></a><a id="cert_chain_revocation_check_end_cert"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_END_CERT</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Revocation checking is done on the end certificate and only the end certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_CHAIN"></a><a id="cert_chain_revocation_check_chain"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_CHAIN</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Revocation checking is done on all of the certificates in every chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT"></a><a id="cert_chain_revocation_check_chain_exclude_root"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Revocation checking is done on all certificates in all of the chains except the root certificate.

</td>
</tr>
</table>
 


### -param pvReserved [in]

This parameter is reserved and must be <b>NULL</b>.


### -param ppChainContext [out]

The address of a pointer to the chain context created. When you have finished using the chain context, release the chain by calling the <a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a> function.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns  zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When an application requests a certificate chain, the structure returned is in the form of a 
<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a>. This context contains an array of 
<a href="https://msdn.microsoft.com/c130cab4-bf8d-429a-beb7-04cb5d37d466">CERT_SIMPLE_CHAIN</a> structures where each simple chain goes from an end certificate to a self-signed certificate. The chain context connects simple chains through trust lists. Each simple chain contains the chain of certificates, summary trust information about the chain, and trust information about each certificate element in the chain.

The following remarks apply to strong signature checking:<ul>
<li>
You can enable strong signature checking for this function by setting the <b>pStrongSignPara</b> member of the <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure that is pointed to by the  <i>pChainPara</i> parameter.

</li>
<li>
If a certificate without a strong signature is found in the chain, the <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> and <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. The <i>ppChainContext</i> parameter points to a <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure which, in turn, points to the  <b>CERT_TRUST_STATUS</b> structure.

</li>
<li>
If the chain is strong signed, the public key in the end certificate is checked to determine whether it  satisfies the minimum public key length requirements for a strong signature.  If the condition is not satisfied, the <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> and <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. To disable checking the key length, set the <b>CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG</b> value in the <b>dwStrongSignFlags</b> member of the <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure pointed to by the  <i>pChainPara</i> parameter.

</li>
<li>
If the <b>CERT_STRONG_SIGN_ENABLE_CRL_CHECK</b> or <b>CERT_STRONG_SIGN_ENABLE_OCSP_CHECK</b> flags are set in the <a href="https://msdn.microsoft.com/B89CDF67-4620-47B2-8363-717D284368FD">CERT_STRONG_SIGN_SERIALIZED_INFO</a> structure and a CRL or OCSP response is found without a strong signature, the CRL or OCSP response will be treated as being offline. That is, the <b>CERT_TRUST_IS_OFFLINE_REVOCATION</b> and <b>CERT_TRUST_REVOCATION_STATUS_UNKNOWN</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. Also, the <b>dwRevocationResult</b> member of the <a href="https://msdn.microsoft.com/798aa2d7-bf8a-425f-bc36-98a44ba3a9d6">CERT_REVOCATION_INFO</a> structure is set to <b>NTE_BAD_ALGID</b>.  

</li>
</ul>



#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/960f2bb9-130f-494f-9af0-0ab8ae3eb6e2">Example C Program: Creating a Certificate Chain</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a>



<a href="https://msdn.microsoft.com/fea72a3e-5a22-47c7-8f6e-0d76fc3339f8">CertDuplicateCertificateChain</a>



<a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a>



<a href="cryptography_functions.htm">Certificate Chain Verification Functions</a>
 

 

