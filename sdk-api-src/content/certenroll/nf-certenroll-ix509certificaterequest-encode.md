---
UID: NF:certenroll.IX509CertificateRequest.Encode
title: IX509CertificateRequest::Encode (certenroll.h)
description: Signs and encodes a certificate request and creates a key pair if one does not exist.
helpviewer_keywords: ["Encode","Encode method [Security]","Encode method [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","Encode method","IX509CertificateRequest.Encode","IX509CertificateRequest::Encode","certenroll/IX509CertificateRequest::Encode","security.ix509certificaterequest_encode_method"]
old-location: security\ix509certificaterequest_encode_method.htm
tech.root: security
ms.assetid: 098788f4-539f-420b-a4e1-65625dd56ca1
ms.date: 12/05/2018
ms.keywords: Encode, Encode method [Security], Encode method [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],Encode method, IX509CertificateRequest.Encode, IX509CertificateRequest::Encode, certenroll/IX509CertificateRequest::Encode, security.ix509certificaterequest_encode_method
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
 - IX509CertificateRequest::Encode
 - certenroll/IX509CertificateRequest::Encode
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
 - IX509CertificateRequest.Encode
---

# IX509CertificateRequest::Encode


## -description

The <b>Encode</b> method signs and encodes a certificate request and creates a key pair if one does not exist. The request is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array.  You can retrieve the byte array by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_rawdata">RawData</a> property.



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
<dt><b>CERTSRV_E_ARCHIVED_KEY_REQUIRED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a> property has been set for a CMC request but a key exchange certificate could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>

## -remarks

For a PKCS #10 request, this method:<ul>
<li>Updates the private key or creates the key if necessary.</li>
<li>Populates the public key from the private key.</li>
<li>Updates the extensions, adding any default extensions and taking account of the suppressed OID collection and critical extension OID collection.</li>
<li>Updates the attributes, adding default attributes and taking account of the suppressed OID collection.</li>
<li>Assembles and encodes the unsigned updated request.</li>
<li>Creates and encodes a signature.</li>
<li>Encodes the signature and the unsigned request.</li>
</ul>


For a CMC request, this method:<ul>
<li>Encodes all inner request objects.</li>
<li>Updates the extensions for the outer request object, adding any default extensions and taking account of the suppressed OID collection and critical extension OID collection.</li>
<li>Updates the attributes for the outer request object, adding default attributes and taking account of the suppressed OID collection.</li>
<li>Updates the name-value pair collection.</li>
<li>Encodes the CMC content that consists of the encoded inner request and the updated outer request.</li>
<li>Creates and encodes a signature for each signing certificate.</li>
<li>Creates and encodes a  primary signature.</li>
<li>Assembles the encoded CMC content (including the inner request and the updated outer request) and the encoded signatures.</li>
<li>Encodes the assembled content into a PKCS #7 message.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
