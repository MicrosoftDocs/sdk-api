---
UID: NF:wincrypt.CertSelectCertificateChains
title: CertSelectCertificateChains function (wincrypt.h)
description: Retrieves certificate chains based on specified selection criteria.
helpviewer_keywords: ["CERT_SELECT_ALLOW_DUPLICATES","CERT_SELECT_ALLOW_EXPIRED","CERT_SELECT_DISALLOW_SELFSIGNED","CERT_SELECT_HARDWARE_ONLY","CERT_SELECT_HAS_KEY_FOR_KEY_EXCHANGE","CERT_SELECT_HAS_KEY_FOR_SIGNATURE","CERT_SELECT_HAS_PRIVATE_KEY","CERT_SELECT_TRUSTED_ROOT","CertSelectCertificateChains","CertSelectCertificateChains function [Security]","security.certselectcertificatechains","wincrypt/CertSelectCertificateChains"]
old-location: security\certselectcertificatechains.htm
tech.root: security
ms.assetid: b740772b-d25b-4b3d-9acb-03f7018750d6
ms.date: 12/05/2018
ms.keywords: CERT_SELECT_ALLOW_DUPLICATES, CERT_SELECT_ALLOW_EXPIRED, CERT_SELECT_DISALLOW_SELFSIGNED, CERT_SELECT_HARDWARE_ONLY, CERT_SELECT_HAS_KEY_FOR_KEY_EXCHANGE, CERT_SELECT_HAS_KEY_FOR_SIGNATURE, CERT_SELECT_HAS_PRIVATE_KEY, CERT_SELECT_TRUSTED_ROOT, CertSelectCertificateChains, CertSelectCertificateChains function [Security], security.certselectcertificatechains, wincrypt/CertSelectCertificateChains
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - CertSelectCertificateChains
 - wincrypt/CertSelectCertificateChains
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
 - CertSelectCertificateChains
---

# CertSelectCertificateChains function


## -description

The <b>CertSelectCertificateChains</b> function retrieves certificate chains based on specified selection criteria.

## -parameters

### -param pSelectionContext [in, optional]

A pointer to the GUID of the certificate selection scenario to use for this call.

### -param dwFlags [in]

Flags for controlling the certificate selection process. This parameter can be a combination of zero or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_ALLOW_EXPIRED"></a><a id="cert_select_allow_expired"></a><dl>
<dt><b>CERT_SELECT_ALLOW_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
Select expired certificates that meet selection criteria. By default expired certificates are rejected from selection.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_TRUSTED_ROOT"></a><a id="cert_select_trusted_root"></a><dl>
<dt><b>CERT_SELECT_TRUSTED_ROOT</b></dt>
</dl>
</td>
<td width="60%">
Select certificates on which the error bit in the certificate chain trust status is not set to <b>CERT_TRUST_IS_UNTRUSTED_ROOT</b>, <b>CERT_TRUST_IS_PARTIAL_CHAIN</b>, or <b>CERT_TRUST_IS_NOT_TIME_VALID</b>. 

In addition, certificates that have one of the following invalid constraint errors are not selected:

<ul>
<li><b>CERT_TRUST_INVALID_POLICY_CONSTRAINTS</b></li>
<li><b>CERT_TRUST_INVALID_BASIC_CONSTRAINTS</b></li>
<li><b>CERT_TRUST_INVALID_NAME_CONSTRAINTS</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_DISALLOW_SELFSIGNED"></a><a id="cert_select_disallow_selfsigned"></a><dl>
<dt><b>CERT_SELECT_DISALLOW_SELFSIGNED</b></dt>
</dl>
</td>
<td width="60%">
Select certificates that are not self-issued and self-signed.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_HAS_PRIVATE_KEY"></a><a id="cert_select_has_private_key"></a><dl>
<dt><b>CERT_SELECT_HAS_PRIVATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
Select  certificates that have a value set for the <b>CERT_KEY_PROV_INFO_PROP_ID</b>  property of the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_HAS_KEY_FOR_SIGNATURE"></a><a id="cert_select_has_key_for_signature"></a><dl>
<dt><b>CERT_SELECT_HAS_KEY_FOR_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Select certificates on which the value of the <b>dwKeySpec</b> member of  the  <b>CERT_KEY_PROV_INFO_PROP_ID</b> property is set to <b>AT_SIGNATURE</b>. 

If this function is being called as part of  a CNG enabled application and the <b>dwKeySpec</b> member of  the  <b>CERT_KEY_PROV_INFO_PROP_ID</b> property is set to -1, select certificates on which the value of the <b>NCRYPT_KEY_USAGE_PROPERTY</b> property of the associated private key has the <b>NCRYPT_ALLOW_SIGNING_FLAG</b> set.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_HAS_KEY_FOR_KEY_EXCHANGE"></a><a id="cert_select_has_key_for_key_exchange"></a><dl>
<dt><b>CERT_SELECT_HAS_KEY_FOR_KEY_EXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Select certificates on which the value of the <b>dwKeySpec</b> member of  the  <b>CERT_KEY_PROV_INFO_PROP_ID</b> property is set to <b>AT_KEYEXCHANGE</b>. 

If this function is being called as part of  a CNG enabled application and the <b>dwKeySpec</b> member of  the  <b>CERT_KEY_PROV_INFO_PROP_ID</b> property is set to -1, select certificates on which either <b>NCRYPT_ALLOW_DECRYPT_FLAG</b> or <b>NCRYPT_ALLOW_KEY_AGREEMENT_FLAG</b> is set.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_HARDWARE_ONLY"></a><a id="cert_select_hardware_only"></a><dl>
<dt><b>CERT_SELECT_HARDWARE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Select certificates on which the value of the <b>PP_IMPTYPE</b> property of the associated private key provider is set to either <b>  CRYPT_IMPL_HARDWARE</b> or <b>CRYPT_IMPL_REMOVABLE</b>. (For CNG providers, NCRYPT_IMPL_TYPE_PROPERTY property value MUST have either the NCRYPT_IMPL_HARDWARE_FLAG or NCRYPT_IMPL_REMOVABLE_FLAG bit set).

If this function is being called as part of  a CNG enabled application, select certificates on which the <b>NCRYPT_IMPL_TYPE_PROPERTY</b> property is set to <b> NCRYPT_IMPL_HARDWARE_FLAG</b> or <b>NCRYPT_IMPL_REMOVABLE_FLAG</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_ALLOW_DUPLICATES"></a><a id="cert_select_allow_duplicates"></a><dl>
<dt><b>CERT_SELECT_ALLOW_DUPLICATES</b></dt>
</dl>
</td>
<td width="60%">
Allow the selection of certificates on which the Subject and Subject Alt Name contain the same information  and the certificate template extension value is equivalent.  By default when certificates match this criteria, only the most recent certificate is selected.

</td>
</tr>
</table>

### -param pChainParameters [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_chain_para">CERT_SELECT_CHAIN_PARA</a> structure to specify parameters for chain building. If <b>NULL</b>, default parameters will be used.

The <b>pChainPara</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_chain_para">CERT_SELECT_CHAIN_PARA</a> structure points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure that can be used to enable strong signing.

### -param cCriteria [in]

The number of elements in the array pointed to by the <i>rgpCriteria</i> array.

### -param rgpCriteria [in, optional]

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_criteria">CERT_SELECT_CRITERIA</a> structures that define the selection criteria. If this parameter is set to <b>NULL</b>, the value of the <i>cCriteria</i> parameter must be zero.

### -param hStore [in]

The handle to a store from which to select the certificates.

### -param pcSelection [out]

 A pointer to a <b>DWORD</b> value to receive the number of elements in the array pointed to by the <i>pprgpSelection</i> parameter.

### -param pprgpSelection [out]

A pointer to a pointer to a location to receive an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structure. The <b>CertSelectCertificateChains</b> function only returns certificate chains that match all the selection criteria. The entries in the array are ordered by quality, i.e. the chain with the highest quality is the first entry. 

Storage for the array is allocated by the <b>CertSelectCertificateChains</b> function. To free the allocated memory you must first release each individual chain context in the array by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain">CertFreeCertificateChain</a> function. Then you must  free the memory by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechainlist">CertFreeCertificateChainList</a> function.

## -returns

If the function succeeds, the function returns <b>TRUE</b>. 

If the function fails, it returns zero (FALSE). For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


<div class="alert"><b>Note</b>  If the selection does not yield any results, the <b>CertSelectCertificateChains</b> function returns <b>TRUE</b>, but the value pointed to by <i>pcSelection</i> parameter is set to zero.
</div>
<div> </div>

## -remarks

Selection criteria can  be specified through either the  <i>dwFlags</i>  parameter, through the <i>rgpCriteria</i> parameter, or through both parameters. If no selection criteria are specified, the function  succeeds and returns certificate chains for all certificates in the store specified by the <i>hStore</i> parameter.


Certificate chains that are selected are ordered based on the following preference logic:

<ul>
<li>Prefer certificates that are smart card certificates over certificates that are not smart-card based.</li>
<li>Prefer certificates that have a longer validity period (the expiration date is later.)</li>
<li>If multiple certificates have same expiration date, prefer certificates that were issued more recently.</li>
<li>If there is a tie, prefer shorter chains.</li>
</ul>
Certain selection criteria require that a certificate chain be built before you can select that criteria for use. If the intermediate certificates required to build the chain are not available locally, a network retrieval is performed for the issuer certificates. This network retrieval is performed if the <b>CERT_SELECT_TRUSTED_ROOT</b> flag is set or for the following criteria:

<ul>
<li><b>CERT_SELECT_BY_ISSUER_NAME</b></li>
<li><b>CERT_SELECT_BY_ISSUER_ATTR</b></li>
<li><b>CERT_SELECT_BY_POLICY_OID</b></li>
</ul>
Perform the following actions to enable strong signature checking:<ul>
<li>Create a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure, specify the required strong signing parameters, and set a pointer to the structure in the <b>pStrongSignPara</b> member of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure.</li>
<li>Set a pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure in the <b>pChainPara</b> member of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_chain_para">CERT_SELECT_CHAIN_PARA</a> structure.</li>
<li>Set  a pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_chain_para">CERT_SELECT_CHAIN_PARA</a> structure in the <i>pChainParameters</i> parameter of this (<b>CertSelectCertificateChains</b>)function.</li>
</ul>


When you enable strong signature checking, any certificate chain that returns a <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> error in the <b>dwErrorStatus</b> field of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a> structure will be skipped. (The <i>pprgpSelection</i> parameter points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structure which, in turn, points to the  <b>CERT_TRUST_STATUS</b> structure.) The <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> value is also set for a weak signature.

## -see-also

<b></b>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>