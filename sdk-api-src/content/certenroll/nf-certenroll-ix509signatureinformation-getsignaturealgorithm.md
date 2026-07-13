---
UID: NF:certenroll.IX509SignatureInformation.GetSignatureAlgorithm
title: IX509SignatureInformation::GetSignatureAlgorithm (certenroll.h)
description: Retrieves the signing algorithm object identifier (OID).
helpviewer_keywords: ["GetSignatureAlgorithm","GetSignatureAlgorithm method [Security]","GetSignatureAlgorithm method [Security]","IX509SignatureInformation interface","IX509SignatureInformation interface [Security]","GetSignatureAlgorithm method","IX509SignatureInformation.GetSignatureAlgorithm","IX509SignatureInformation::GetSignatureAlgorithm","certenroll/IX509SignatureInformation::GetSignatureAlgorithm","security.ix509signatureinformation_getsignaturealgorithm_method"]
old-location: security\ix509signatureinformation_getsignaturealgorithm_method.htm
tech.root: security
ms.assetid: e5b43e74-d802-43ff-bdf2-96ab475c31e7
ms.date: 12/05/2018
ms.keywords: GetSignatureAlgorithm, GetSignatureAlgorithm method [Security], GetSignatureAlgorithm method [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],GetSignatureAlgorithm method, IX509SignatureInformation.GetSignatureAlgorithm, IX509SignatureInformation::GetSignatureAlgorithm, certenroll/IX509SignatureInformation::GetSignatureAlgorithm, security.ix509signatureinformation_getsignaturealgorithm_method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509SignatureInformation::GetSignatureAlgorithm
 - certenroll/IX509SignatureInformation::GetSignatureAlgorithm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509SignatureInformation.GetSignatureAlgorithm
---

# IX509SignatureInformation::GetSignatureAlgorithm


## -description

The <b>GetSignatureAlgorithm</b> method retrieves the signing algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param Pkcs7Signature [in]

A <b>VARIANT_BOOL</b> variable that specifies whether the algorithm will be used to sign a PKCS #7 or CMC certificate request.

### -param SignatureKey [in]

A <b>VARIANT_BOOL</b> variable that specifies whether an algorithm that is only used for signing is preferred when an algorithm OID is associated with more than one purpose. For example, XCN_OID_RSA_RSA (1.2.840.113549.1.1.1) can be used for both signing and key exchange.

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the algorithm OID.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The hashing algorithm  OID, or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> property has not been specified but the signing algorithm OID cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The combined signature algorithm could not be found.

</td>
</tr>
</table>

## -remarks

This method searches for a cached signing algorithm that is consistent with the input parameters. If none is found, the method uses the input parameters plus the values assigned to various <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> properties as indicated by the following list.<ul>
<li>
<i>Pkcs7Signature</i> = true, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> = true

This case represents a null-signed PKCS #7 certificate request.  The method returns the XCN_OID_PKIX_NO_SIGNATURE (1.3.6.1.5.5.7.6.2) OID.

</li>
<li>
<i>Pkcs7Signature</i> = true, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> = false

This case retrieves  a discrete signature algorithm OID for a PKCS #7 request that is not null-signed. The discrete signature requires that the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm">HashAlgorithm</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> properties be set. In the special case where  the public key algorithm is XCN_OID_X957_DSA and the hashing algorithm is not XCN_OID_OIWSEC_sha1, the signature algorithm OID retrieved is XCN_OID_X957_SHA1DSA (1.2.840.10040.4.3).

</li>
<li>
<i>Pkcs7Signature</i> = false, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> = false, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> = true

This case retrieves  a discrete signature algorithm OID for a PKCS #10 request and encodes the hash algorithm OID in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_parameters">Parameters</a> property. The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm">HashAlgorithm</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> properties must be set.

</li>
<li>
<i>Pkcs7Signature</i> = false, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> = false, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> = false

This case retrieves  a discrete signature algorithm OID for a PKCS #7 request. The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm">HashAlgorithm</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> properties must be set.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>