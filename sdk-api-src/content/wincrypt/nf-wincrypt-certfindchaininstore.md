---
UID: NF:wincrypt.CertFindChainInStore
title: CertFindChainInStore function
author: windows-sdk-content
description: Finds the first or next certificate in a store that meets the specified criteria.
old-location: security\certfindchaininstore.htm
tech.root: seccrypto
ms.assetid: 698cece8-71a8-4bfa-8ee6-8035a6dcbe05
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CERT_CHAIN_FIND_BY_ISSUER, CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG, CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG, CERT_CHAIN_FIND_BY_ISSUER_COMPARE_KEY_FLAG, CERT_CHAIN_FIND_BY_ISSUER_COMPLEX_CHAIN_FLAG, CERT_CHAIN_FIND_BY_ISSUER_LOCAL_MACHINE_FLAG, CERT_CHAIN_FIND_BY_ISSUER_NO_KEY_FLAG, CertFindChainInStore, CertFindChainInStore function [Security], X509_ASN_ENCODING, _crypto2_certfindchaininstore, security.certfindchaininstore, wincrypt/CertFindChainInStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFindChainInStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFindChainInStore function


## -description


The <b>CertFindChainInStore</b> function finds the first or next certificate in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">store</a> that meets the specified criteria. It then builds and verifies a certificate chain context for that certificate. The certificate that is found and for which the chain is built is selected according to criteria established by the <i>dwFindFlags</i>, <i>dwFindType</i>, and <i>pvFindPara</i> parameters. This function can be used in a loop to find all of the certificates in a certificate store that match the specified find criteria and to build a certificate chain context for each certificate found.


## -parameters




### -param hCertStore [in]

The handle of the store to be searched for a certificate upon which a chain is built. This handle is passed as an additional store to 
the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> function as the chain is built.


### -param dwCertEncodingType [in]

The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate encoding type</a>   that was used to encode the store. The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


This parameter can be the following currently defined certificate encoding type.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies X.509 certificate encoding.

</td>
</tr>
</table>
 


### -param dwFindFlags [in]

Contains additional options for the search. The possible values for this parameter depend on the value of the <i>dwFindType</i> parameter.


This parameter can contain zero or a combination of one or more of the following values when <i>dwFindType</i> contains <b>CERT_CHAIN_FIND_BY_ISSUER</b>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_COMPARE_KEY_FLAG"></a><a id="cert_chain_find_by_issuer_compare_key_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_COMPARE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Compares the public key in the certificate with the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider's</a> <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>. This comparison is the last check made on the chain when it is built.

Because the <b>hCryptProv</b> member of an issuer contains a private key, it might need to be checked several times during this process; to facilitate this checking, the <i>dwAcquirePrivateKeyFlags</i> member can be set in the <a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a> structure to enable caching of that <b>hCryptProv</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_COMPLEX_CHAIN_FLAG"></a><a id="cert_chain_find_by_issuer_complex_chain_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_COMPLEX_CHAIN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, only the first simple chain is checked for issuer name matches. With this flag set, the default is overridden and subsequent simple chains are also checked for issuer name matches.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG"></a><a id="cert_chain_find_by_issuer_cache_only_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Improves the performance of this function by causing it to search only the cached system stores (Root, My, Ca, Trust) to find issuer certificates. If this flag is not set, the function searches the cached system stores and the store represented by the <i>hCertStore</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG"></a><a id="cert_chain_find_by_issuer_cache_only_url_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Only the URL cache is searched. The Internet is not searched.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_LOCAL_MACHINE_FLAG"></a><a id="cert_chain_find_by_issuer_local_machine_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_LOCAL_MACHINE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Only opens the Local Machine certificate stores. The certificate stores of the current user are not opened.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_FIND_BY_ISSUER_NO_KEY_FLAG"></a><a id="cert_chain_find_by_issuer_no_key_flag"></a><dl>
<dt><b>CERT_CHAIN_FIND_BY_ISSUER_NO_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
No check is made to determine whether the certificate has an associated private key.

</td>
</tr>
</table>
 


### -param dwFindType [in]

Determines what criteria to use to find a certificate in the store.


This parameter can be the following currently defined value.





#### CERT_CHAIN_FIND_BY_ISSUER

Finds the certificate based on the name of the issuer. The <i>pvFindPara</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a> structure that contains members that modify the search.

The certificate chain is built for a certificate with an available <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. By default, only the issuers in the first simple chain are compared in an issuer name match. If this flag is set, all of the chains are checked for an issuer certificate that matches one of a set of issuer names.

This function will compare the name <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOBs</a> passed in the <i>pvFindPara</i> structure to any <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) in the chain, not just the certification authority in the root certificate.

This function does not perform any revocation checks.

If <i>pPrevChainContext</i> is not <b>NULL</b>, this function will return a chain for a different certificate every time the function is called. If there is only one suitable certificate, but there are two matching issuing certificate authorities, one of which is revoked, it is possible for this function to return the revoked chain. If the application then checks for revocation itself through calls to the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function and finds the chain unsuitable, an additional call to the <b>CertFindChainInStore</b> function will not return a chain that includes the same certificate from the valid certification authority. It will instead return a completely different chain with a different certificate or <b>NULL</b>, if no such chain can be found.


### -param pvFindPara [in]

A pointer that contains additional search criteria. The type and format of the data this parameter points to depends on the value of the <i>dwFindType</i> parameter.


### -param pPrevChainContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure returned from a previous call to this function. The search is begun from this certificate. For the first call to this function, this parameter must be <b>NULL</b>. In subsequent calls, it is the pointer returned by the previous call to the function.  If this parameter is not <b>NULL</b>, this function will free this structure.


## -returns



If the first or next chain context is not built, <b>NULL</b> is returned. Otherwise, a pointer to a read-only <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure is returned. The <b>CERT_CHAIN_CONTEXT</b> structure is freed when passed as the <i>pPrevChainContext</i> parameter on a subsequent call to this function. Otherwise, the <b>CERT_CHAIN_CONTEXT</b> structure must be freed explicitly by calling 
the <a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a> function.




## -remarks



The <i>pPrevChainContext</i> parameter must be <b>NULL</b> on the first call to build the chain context. To build the next chain context, the <i>pPrevChainContext</i> is set to the <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure returned by a previous call. If <i>pPrevChainContext</i> is not <b>NULL</b>, the structure is always freed by this function by using the <a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a> function, even if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a>



<a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a>



<a href="https://msdn.microsoft.com/5ba181c2-6936-4848-a571-2bb58f46f081">CertFreeCertificateChain</a>



<a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>



<a href="cryptography_functions.htm">Certificate Chain Verification Functions</a>
 

 

