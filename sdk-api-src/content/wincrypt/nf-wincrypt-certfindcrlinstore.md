---
UID: NF:wincrypt.CertFindCRLInStore
title: CertFindCRLInStore function (wincrypt.h)
description: Finds the first or next certificate revocation list (CRL) context in a certificate store that matches a search criterion established by the dwFindType parameter and the associated pvFindPara parameter.
helpviewer_keywords: ["CRL_FIND_ANY","CRL_FIND_EXISTING","CRL_FIND_ISSUED_BY","CRL_FIND_ISSUED_BY_AKI_FLAG","CRL_FIND_ISSUED_BY_BASE_FLAG","CRL_FIND_ISSUED_BY_DELTA_FLAG","CRL_FIND_ISSUED_BY_SIGNATURE_FLAG","CRL_FIND_ISSUED_FOR","CRL_FIND_ISSUED_FOR_SET_STRONG_PROPERTIES_FLAG","CertFindCRLInStore","CertFindCRLInStore function [Security]","_crypto2_certfindcrlinstore","security.certfindcrlinstore","wincrypt/CertFindCRLInStore"]
old-location: security\certfindcrlinstore.htm
tech.root: security
ms.assetid: 3e481912-204a-4d86-ab67-81f8ae4d1aaa
ms.date: 12/05/2018
ms.keywords: CRL_FIND_ANY, CRL_FIND_EXISTING, CRL_FIND_ISSUED_BY, CRL_FIND_ISSUED_BY_AKI_FLAG, CRL_FIND_ISSUED_BY_BASE_FLAG, CRL_FIND_ISSUED_BY_DELTA_FLAG, CRL_FIND_ISSUED_BY_SIGNATURE_FLAG, CRL_FIND_ISSUED_FOR, CRL_FIND_ISSUED_FOR_SET_STRONG_PROPERTIES_FLAG, CertFindCRLInStore, CertFindCRLInStore function [Security], _crypto2_certfindcrlinstore, security.certfindcrlinstore, wincrypt/CertFindCRLInStore
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
 - CertFindCRLInStore
 - wincrypt/CertFindCRLInStore
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
 - CertFindCRLInStore
---

# CertFindCRLInStore function


## -description

The <b>CertFindCRLInStore</b> function finds the first or next <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that matches a search criterion established by the <i>dwFindType</i> parameter and the associated <i>pvFindPara</i> parameter. This function can be used in a loop to find all of the CRL contexts in a certificate store that match the specified find criteria.

## -parameters

### -param hCertStore [in]

A handle of the certificate store to be searched.

### -param dwCertEncodingType [in]

This parameter is not currently used. It must be set to zero.

### -param dwFindFlags [in]

If <i>dwFindType</i> is CRL_FIND_ISSUED_BY, by default, only issuer name matching is done. The following flags can be used to do additional filtering.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_BY_AKI_FLAG"></a><a id="crl_find_issued_by_aki_flag"></a><dl>
<dt><b>CRL_FIND_ISSUED_BY_AKI_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Checks for a CRL that has an Authority Key Identifier (AKI) extension. If the CRL has an AKI, only a CRL whose AKI matches the issuer is returned.

<div class="alert"><b>Note</b>  The AKI extension has the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) value szOID_AUTHORITY_KEY_IDENTIFIER2 and its corresponding data structure.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_BY_SIGNATURE_FLAG"></a><a id="crl_find_issued_by_signature_flag"></a><dl>
<dt><b>CRL_FIND_ISSUED_BY_SIGNATURE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Use the public key in the issuer's certificate to verify the signature on the CRL. Only returns a CRL that has a valid signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_BY_DELTA_FLAG"></a><a id="crl_find_issued_by_delta_flag"></a><dl>
<dt><b>CRL_FIND_ISSUED_BY_DELTA_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Finds and returns a delta CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_BY_BASE_FLAG"></a><a id="crl_find_issued_by_base_flag"></a><dl>
<dt><b>CRL_FIND_ISSUED_BY_BASE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Finds and returns a base CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_FOR_SET_STRONG_PROPERTIES_FLAG"></a><a id="crl_find_issued_for_set_strong_properties_flag"></a><dl>
<dt><b>CRL_FIND_ISSUED_FOR_SET_STRONG_PROPERTIES_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The signature is checked for strength after successful verification. This flag applies only when the <i>dwFindType</i> parameter is set to <b>CRL_FIND_ISSUED_FOR</b>. You must also set <b>CRL_FIND_ISSUED_BY_SIGNATURE_FLAG</b>. If successful, the following strong signature properties will be set on the CRL context:

<ul>
<li><b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b></li>
<li><b>CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID</b></li>
</ul>
<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>

### -param dwFindType [in]

Specifies the type of search being made. The value of <i>dwFindType</i> determines the data type, contents, and use of the <i>pvFindPara</i> parameter. Currently defined search types and their <i>pvFindPara</i> requirements are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ANY"></a><a id="crl_find_any"></a><dl>
<dt><b>CRL_FIND_ANY</b></dt>
<dt>The <i>pvFindPara</i> parameter is not used. It must be set to <b>NULL</b>.</dt>
</dl>
</td>
<td width="60%">
No search criteria. The next CRL in the store is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_BY"></a><a id="crl_find_issued_by"></a><dl>
<dt><b>CRL_FIND_ISSUED_BY</b></dt>
<dt>A pointer to a CERT_CONTEXT.</dt>
</dl>
</td>
<td width="60%">
Searches for the next CRL in the store matching the issuer in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_EXISTING"></a><a id="crl_find_existing"></a><dl>
<dt><b>CRL_FIND_EXISTING</b></dt>
<dt>A pointer to a CRL_CONTEXT.</dt>
</dl>
</td>
<td width="60%">
Searches for the next CRL that matches the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> in the following ways:

<ul>
<li> Both are base or delta CRLs.</li>
<li>The issuer-name BLOBs for both are identical.</li>
<li>If they exist, the Authority/KeyIdentifier and IssuingDistributionPoint encoded extension BLOBs match.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CRL_FIND_ISSUED_FOR"></a><a id="crl_find_issued_for"></a><dl>
<dt><b>CRL_FIND_ISSUED_FOR</b></dt>
<dt>A pointer to a CRL_FIND_ISSUED_FOR_PARA.</dt>
</dl>
</td>
<td width="60%">
Searches for the next CRL in the store that matches the issuer of the subject certificate in the CRL_FIND_ISSUED_FOR_PARA structure.

If no CRL is found, searches for the next CRL in the store that matches the issuer in the CRL_FIND_ISSUED_FOR_PARA structure.

<div class="alert"><b>Note</b>  When using cross certificates, the subject name in the issuer's certificate might not match the issuer name in the subject certificate and its corresponding CRL.</div>
<div> </div>
</td>
</tr>
</table>

### -param pvFindPara [in]

This parameter is determined by the value of <i>dwFindType</i>. For details, see the table earlier in this topic.

### -param pPrevCrlContext [in]

A pointer to the last 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> returned by this function. Must be <b>NULL</b> to get the first CRL in the store meeting the search criteria. Successive CRLs meeting the search criteria can be found by setting <i>pPrevCrlContext</i> to the <b>PCCRL_CONTEXT</b> pointer returned by a previous call to the function. The search process skips any CRLs that do not match the search criteria or that have been previously deleted from the store by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a>. This function frees the <b>CRL_CONTEXT</b> referenced by values of this parameter that are not <b>NULL</b>.

## -returns

If the function succeeds, the function returns a pointer to a read-only CRL context. When you have finished using the returned CRL context, free it by calling 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> function or implicitly free it by passing it as the <i>pPrevCrlContext</i> parameter on a subsequent call to the <b>CertFindCRLInStore</b> function.
						
						

If the function fails and a CRL that matches the search criteria is not found, the return value is <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CRL context pointed to by the <i>pPrevCrlContext</i> parameter, or a search type that is not valid was specified in the <i>dwFindType</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No CRLs are in the store, no CRL was found that matched the search criteria, or the end of the store's list was reached.

</td>
</tr>
</table>

## -remarks

The returned pointer is freed when passed as the <i>pPrevCrlContext</i> parameter on a subsequent call to the function. Otherwise, the pointer must be explicitly freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>. A <i>pPrevCrlContext</i> that is not <b>NULL</b> is always freed by <b>CertFindCRLInStore</b> using a call to <b>CertFreeCRLContext</b>, even if there is an error in the function.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a> can be called to make a duplicate of the returned context. The returned CRL context can be added to a different certificate store by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>, or a link to that CRL context can be added to a noncollection store by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrllinktostore">CertAddCRLLinkToStore</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrllinktostore">CertAddCRLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>