---
UID: NF:wincrypt.CertVerifyRevocation
title: CertVerifyRevocation function (wincrypt.h)
description: Checks the revocation status of the certificates contained in the rgpvContext array. If a certificate in the list is found to be revoked, no further checking is done.
helpviewer_keywords: ["CERT_VERIFY_CACHE_ONLY_BASED_REVOCATION","CERT_VERIFY_REV_ACCUMULATIVE_TIMEOUT_FLAG","CERT_VERIFY_REV_CHAIN_FLAG","CERT_VERIFY_REV_SERVER_OCSP_FLAG","CertVerifyRevocation","CertVerifyRevocation function [Security]","_crypto2_certverifyrevocation","security.certverifyrevocation","wincrypt/CertVerifyRevocation"]
old-location: security\certverifyrevocation.htm
tech.root: security
ms.assetid: 2d6fb244-5273-4530-bec4-e5451fe26f2e
ms.date: 12/05/2018
ms.keywords: CERT_VERIFY_CACHE_ONLY_BASED_REVOCATION, CERT_VERIFY_REV_ACCUMULATIVE_TIMEOUT_FLAG, CERT_VERIFY_REV_CHAIN_FLAG, CERT_VERIFY_REV_SERVER_OCSP_FLAG, CertVerifyRevocation, CertVerifyRevocation function [Security], _crypto2_certverifyrevocation, security.certverifyrevocation, wincrypt/CertVerifyRevocation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertVerifyRevocation
 - wincrypt/CertVerifyRevocation
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
 - CertVerifyRevocation
---

# CertVerifyRevocation function


## -description

The <b>CertVerifyRevocation</b> function checks the revocation status of the certificates contained in the <i>rgpvContext</i> array. If a certificate in the list is found to be revoked, no further checking is done. This array can be a chain of certificates propagating upward from an end entity to the <a href="/windows/desktop/SecGloss/r-gly">root authority</a>, but this nature of the list of certificates is not required or assumed.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param dwRevType [in]

Indicates the type of the context structure passed in <i>rgpvContext</i>. Currently only CERT_CONTEXT_REVOCATION_TYPE, the revocation of certificates, is defined.

### -param cContext [in]

Count of elements in the <i>rgpvContext</i> array.

### -param rgpvContext [in]

When the <i>dwRevType</i> is CERT_CONTEXT_REVOCATION_TYPE, <i>rgpvContext</i> is an array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures. These contexts must contain sufficient information to allow the installable or registered revocation DLLs to find the revocation server. This information would normally be conveyed in an extension such as the CRLDistributionsPoints extension defined by the Internet Engineering Task Force (IETF) in PKIX Part 1. 




For efficiency, the more contexts that are passed in at one time, the better.

### -param dwFlags [in]

Indicates any special processing needs. This parameter can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_VERIFY_REV_CHAIN_FLAG"></a><a id="cert_verify_rev_chain_flag"></a><dl>
<dt><b>CERT_VERIFY_REV_CHAIN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Verification of the chain of certificates is done assuming each certificate except the first certificate is the issuer of the certificate that precedes it. If <i>dwRevType</i> is not CERT_CONTEXT_REVOCATION_TYPE, no assumptions are made about the order of the contexts.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_VERIFY_CACHE_ONLY_BASED_REVOCATION"></a><a id="cert_verify_cache_only_based_revocation"></a><dl>
<dt><b>CERT_VERIFY_CACHE_ONLY_BASED_REVOCATION</b></dt>
</dl>
</td>
<td width="60%">
Prevents the revocation handler from accessing any network-based resources for revocation checking.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_VERIFY_REV_ACCUMULATIVE_TIMEOUT_FLAG"></a><a id="cert_verify_rev_accumulative_timeout_flag"></a><dl>
<dt><b>CERT_VERIFY_REV_ACCUMULATIVE_TIMEOUT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When set, <b>dwUrlRetrievalTimeout</b> is the cumulative time-out across all URL wire retrievals.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_VERIFY_REV_SERVER_OCSP_FLAG"></a><a id="cert_verify_rev_server_ocsp_flag"></a><dl>
<dt><b>CERT_VERIFY_REV_SERVER_OCSP_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When set, this function only uses <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) for revocation checking. If the certificate does not have any OCSP AIA URLs, the <b>dwError</b> member of the <i>pRevStatus</i> parameter is set to CRYPT_E_NOT_IN_REVOCATION_DATABASE.

</td>
</tr>
</table>

### -param pRevPara [in, optional]

Optionally set to assist in finding the issuer. For details, see the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_para">CERT_REVOCATION_PARA</a> structure.

### -param pRevStatus [in, out]

Only the <b>cbSize</b> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a> pointed to by <i>pRevStatus</i> needs to be set before <b>CertVerifyRevocation</b> is called.

If the function returns <b>FALSE</b>, this structure's members will contain error status information. For more information, see 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a>. For a description of how <i>pRevStatus</i> is updated when a revocation verification problem is encountered, see Remarks.

## -returns

If the function successfully checks all of the contexts and none were revoked, the function returns <b>TRUE</b>. If the function fails, it returns <b>FALSE</b> and updates the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a> structure pointed to by <i>pRevStatus</i> as described in 
<b>CERT_REVOCATION_STATUS</b>.

When the revocation handler for any of the contexts returns <b>FALSE</b> due to an error, the <b>dwError</b> member in the structure pointed to by <i>pRevStatus</i> will be set by the handler to specify which error was encountered. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns an error code equal to the error specified in the <b>dwError</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a> structure. <b>GetLastError</b> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_REVOCATION_CHECK</b></dt>
</dl>
</td>
<td width="60%">
An installed or registered revocation function was not able to do a revocation check on the context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_REVOCATION_DLL</b></dt>
</dl>
</td>
<td width="60%">
No installed or registered DLL was found that was able to verify revocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_IN_REVOCATION_DATABASE</b></dt>
</dl>
</td>
<td width="60%">
The context to be checked was not found in the revocation server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_REVOCATION_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
It was not possible to connect to the revocation server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The context was revoked. <b>dwReason</b> in <i>pRevStatus</i> contains the reason for revocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The context was good.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>cbSize</b> in <i>pRevStatus</i> is less than sizeof(<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a>). Note that <b>dwError</b> in <i>pRevStatus</i> is not updated for this error.

</td>
</tr>
</table>

## -remarks

The following example shows how <i>pRevStatus</i> is updated when a revocation verification problem is encountered:

Consider the case where <i>cContext</i> is four: 

If <b>CertVerifyRevocation</b> can verify that <i>rgpvContext</i>[0] and <i>rgpvContext</i>[1] are not revoked, but cannot check <i>rgpvContext</i>[2], the <i>pRevStatus</i> member <b>dwIndex</b> is set to two, indicating that the context at index two has the problem, the <b>dwError</b> member of <i>pRevStatus</i> is set to CRYPT_E_NO_REVOCATION_CHECK, and <b>FALSE</b> is returned.

If <i>rgpvContext</i>[2] is found to be revoked, the <b>dwIndex</b> member of <i>pRevStatus</i> is set to two, and the <b>dwError</b> member of <i>pRevStatus</i> is set to CRYPT_E_REVOKED, <b>dwReason</b> is updated, and <b>FALSE</b> is returned.

 In either case, both <i>rgpvContext</i>[0] and <i>rgpvContext</i>[1] are verified not to be revoked, <i>rgpvContext</i>[2] is the last array index checked, and <i>rgpvContext</i>[3] has not been checked at all.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_para">CERT_REVOCATION_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_status">CERT_REVOCATION_STATUS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrltimevalidity">CertVerifyCRLTimeValidity</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifytimevalidity">CertVerifyTimeValidity</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyvaliditynesting">CertVerifyValidityNesting</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>