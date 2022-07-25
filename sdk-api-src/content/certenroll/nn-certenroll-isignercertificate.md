---
UID: NN:certenroll.ISignerCertificate
title: ISignerCertificate (certenroll.h)
description: Represents a signing certificate that enables you to sign a certificate request.
helpviewer_keywords: ["ISignerCertificate","ISignerCertificate interface [Security]","ISignerCertificate interface [Security]","described","certenroll/ISignerCertificate","security.isignercertificate"]
old-location: security\isignercertificate.htm
tech.root: security
ms.assetid: 146a1925-4de6-492c-8014-612c65bd7270
ms.date: 12/05/2018
ms.keywords: ISignerCertificate, ISignerCertificate interface [Security], ISignerCertificate interface [Security],described, certenroll/ISignerCertificate, security.isignercertificate
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
 - ISignerCertificate
 - certenroll/ISignerCertificate
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
 - ISignerCertificate
---

# ISignerCertificate interface


## -description

The <b>ISignerCertificate</b> interface represents a signing <a href="/windows/desktop/SecGloss/c-gly">certificate</a> that enables you to sign a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. When you initialize the interface, the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated <a href="/windows/desktop/SecGloss/p-gly">private key</a>. You can use the private key to sign a PKCS #7 or a CMC request but not a PKCS #10 request. PKCS #10 requests must be signed by using the private key associated with the <a href="/windows/desktop/SecGloss/p-gly">public key</a> included in the request. Self-signed certificates can be signed by using the private key associated with the request or the private key associated with the signing certificate. This is summarized in the following table.<table>
<tr>
<th>Request type (Interface)</th>
<th>Signing certificates</th>
</tr>
<tr>
<td>PKCS #7(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>)

</td>
<td>1</td>
</tr>
<tr>
<td>PKCS #10(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10)</a>


</td>
<td>0</td>
</tr>
<tr>
<td>CMC(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>)

</td>
<td>0 or more</td>
</tr>
<tr>
<td>Self-signed(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>)

</td>
<td>0 or 1</td>
</tr>
</table>
 



When signing a CMC request, the data to be signed consists of a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded <b>CmcData</b> object wrapped in a CMS <b>SignedData</b> object. The <b>encryptedDigest</b> field of the <b>SignerInfo</b> object contains a signature, and multiple <b>SignerInfo</b> objects can be associated with the request.

``` syntax

---------------------------------------------------------------------
-- CMC request data
---------------------------------------------------------------------

CmcData ::= SEQUENCE 
{
controlSequence     SEQUENCE OF TaggedAttribute,
reqSequence         SEQUENCE OF TaggedRequest,
cmsSequence         SEQUENCE OF TaggedContentInfo,
otherMsgSequence    SEQUENCE OF TaggedOtherMs
}

---------------------------------------------------------------------
-- SignedData object that wraps the CMC request
---------------------------------------------------------------------

SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

DigestAlgorithmIdentifiers ::=  SET OF DigestAlgorithmIdentifier 
DigestAlgorithmIdentifiersNC ::= SET OF DigestAlgorithmIdentifierNC

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes OPTIONAL
}

```
Each <b>ISignerCertificate</b> object is associated with one <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object that identifies the hashing and public key algorithms used. This object is created and initialized when the <b>ISignerCertificate</b> object is initialized.

## -inheritance

The <b>ISignerCertificate</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISignerCertificate</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a>
