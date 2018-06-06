---
UID: NS:wincrypt._CERT_CHAIN_PARA
title: "_CERT_CHAIN_PARA"
author: windows-sdk-content
description: The CERT_CHAIN_PARA structure establishes the searching and matching criteria to be used in building a certificate chain.
old-location: security\cert_chain_para.htm
old-project: SecCrypto
ms.assetid: 86094e1c-be59-4a15-a05b-21769f80e653
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCERT_CHAIN_PARA, CERT_CHAIN_PARA, CERT_CHAIN_PARA structure [Security], CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG, PCERT_CHAIN_PARA, PCERT_CHAIN_PARA structure pointer [Security], _CERT_CHAIN_PARA, _crypto2_cert_chain_para, security.cert_chain_para, wincrypt/CERT_CHAIN_PARA, wincrypt/PCERT_CHAIN_PARA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CERT_CHAIN_PARA, *PCERT_CHAIN_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_CHAIN_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_CHAIN_PARA structure


## -description


The <b>CERT_CHAIN_PARA</b> structure establishes the searching and matching criteria to be used in building a certificate chain.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field RequestedUsage

Structure indicating the kind of matching necessary to find issuer certificates for building a certificate chain. The structure pointed to indicates whether AND or OR logic is to be used in the matching process. The structure also includes an array of OIDs to be matched.


### -field RequestedIssuancePolicy

Optional structure that indicates the kind of issuance policy constraint matching that applies when building a certificate chain. The structure pointed to indicates whether AND or OR logic is to be used in the matching process. The structure also includes an array of OIDs to be matched.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field dwUrlRetrievalTimeout

Optional time, in milliseconds, before revocation checking times out. This member is optional.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field fCheckRevocationFreshnessTime

Optional member. When this flag is <b>TRUE</b>, an attempt is made to retrieve a new CRL if this update is greater than or equal to the current system time minus the <b>dwRevocationFreshnessTime</b> value. If this flag is not set, the CRL's next update time is used.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field dwRevocationFreshnessTime

The current time, in seconds, minus the CRL's update time of all elements checked.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field pftCacheResync

Optional member. When set to a non-<b>NULL</b>  value, information cached before  the time specified is considered to be not valid and cache resynchronization is performed.

<b>Windows Vista:  </b>Support for this member begins.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field pStrongSignPara

Optional. Specify a pointer to a <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure to enable strong signature checking.

<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

### -field dwStrongSignFlags

Optional flags that modify chain retrieval behavior. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG"></a><a id="cert_chain_strong_sign_disable_end_check_flag"></a><dl>
<dt><b>CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If the chain is strong signed, the public key in the end certificate will be checked to verify whether it satisfies the minimum public key length requirements for a strong signature. You can specify <b>CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG</b> to disable default checking.

</td>
</tr>
</table>
 

<b>Windows 8 and Windows Server 2012:  </b>Support for this property begins.

<div class="alert"><b>Note</b>  This member can be used only if <b>CERT_CHAIN_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If this value is defined, the application must zero all unused fields.</div>
<div> </div>

## -remarks



The following remarks apply when checking for strong signatures.

<ul>
<li>
Set the <b>pStrongSignPara</b> member to check for strong signatures when using the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> or <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> function.

</li>
<li>
If a certificate without a strong signature is found in the chain, the <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> and <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. The <i>ppChainContext</i> parameter of the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> function and the <i>pprgpSelection</i> parameter of the <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> function point to a <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structure which, in turn, points to the  <b>CERT_TRUST_STATUS</b> structure.

</li>
<li>
If the chain is strong signed, the public key in the end certificate is checked to determine whether it  satisfies the minimum public key length requirements for a strong signature.  If the condition is not satisfied, the <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> and <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. Set the <b>CERT_CHAIN_STRONG_SIGN_DISABLE_END_CHECK_FLAG</b> value in the <b>dwStrongSignFlags</b> member to disable this check.

</li>
<li>
If the <b>CERT_STRONG_SIGN_ENABLE_CRL_CHECK</b> or <b>CERT_STRONG_SIGN_ENABLE_OCSP_CHECK</b> flags are set in the <a href="https://msdn.microsoft.com/B89CDF67-4620-47B2-8363-717D284368FD">CERT_STRONG_SIGN_SERIALIZED_INFO</a> structure referenced by the <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure pointed to by the <b>pStrongSignPara</b> member, and a CRL or OCSP response is found without a strong signature, the CRL or OCSP response will be treated as being offline. That is, the <b>CERT_TRUST_IS_OFFLINE_REVOCATION</b> and <b>CERT_TRUST_REVOCATION_STATUS_UNKNOWN</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a> structure. Also, the <b>dwRevocationResult</b> member of the <a href="https://msdn.microsoft.com/798aa2d7-bf8a-425f-bc36-98a44ba3a9d6">CERT_REVOCATION_INFO</a> structure is set to <b>NTE_BAD_ALGID</b>.  

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6154f1f7-4293-4b8e-91ab-9f57bb6f5743">CERT_USAGE_MATCH</a>
 

 

