---
UID: NN:certenroll.IX509CertificateRequestPkcs7
title: IX509CertificateRequestPkcs7 (certenroll.h)
description: The IX509CertificateRequestPkcs7 interface represents a PKCS
helpviewer_keywords: ["IX509CertificateRequestPkcs7","IX509CertificateRequestPkcs7 interface [Security]","IX509CertificateRequestPkcs7 interface [Security]","described","certenroll/IX509CertificateRequestPkcs7","security.ix509certificaterequestpkcs7"]
old-location: security\ix509certificaterequestpkcs7.htm
tech.root: security
ms.assetid: ae869557-6523-4387-835e-c9631898d864
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs7, IX509CertificateRequestPkcs7 interface [Security], IX509CertificateRequestPkcs7 interface [Security],described, certenroll/IX509CertificateRequestPkcs7, security.ix509certificaterequestpkcs7
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
 - IX509CertificateRequestPkcs7
 - certenroll/IX509CertificateRequestPkcs7
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
 - IX509CertificateRequestPkcs7
---

# IX509CertificateRequestPkcs7 interface


## -description

The <b>IX509CertificateRequestPkcs7</b> interface represents a  PKCS #7 certificate message syntax (CMS) object. PKCS #7 defines the format of messages sent to a certification or registration authority to request a public-key certificate.  The <b>IX509CertificateRequestPkcs7</b> interface can be confusing because its implementation does not perfectly mirror the way most security professionals think about the PKCS #7 standard. To avoid this confusion, keep the following points in mind:


<ul>
<li>Although a PKCS #7 message is used to wrap a CMC request, an <b>IX509CertificateRequestPkcs7</b> object cannot contain a <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object. Instead, the <b>IX509CertificateRequestCmc</b> interface inherits and implements the <b>IX509CertificateRequestPkcs7</b> interface. As implemented, a CMC request is therefore a PKCS #7 <b>SignedData</b> object that contains CMC content, a primary signature that is either null-signed or key-based, and zero or more certificate-based signatures. By contrast, a PKCS #7 request is a <b>SignedData</b> object that contains PKCS #10 content (see the next item in this list) and has exactly one certificate-based signature.</li>
<li>An <b>IX509CertificateRequestPkcs7</b> must contain an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object. The main advantage of wrapping a PKCS #10 request in a PKCS #7 message is the ability to add multiple signers. The PKCS #10 request is signed by the associated private key, and the PKCS #7 message that wraps the PKCS #10 request is also signed. This second signer uses the certificate being renewed (for a renewal request) or the enrollment agent certificate (for an enroll-on-behalf-of request).</li>
<li>You can create and enroll a stand-alone <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> certificate request without wrapping it in an <b>IX509CertificateRequestPkcs7</b> object.</li>
</ul>


 The ASN.1 representation of a PKCS #7 object in the following syntax example shows that it can be composed of a variety of data types.

``` syntax

PKCS7ContentTable PKCS7-CONTENT-TYPE ::=
{
    data | signed-data | enveloped-data | signed-and-enveloped-data |
    digested-data | encrypted-data | authenticated-data, ...
}

```
Of these, the <b>SignedData</b> object shown below is most relevant. The <b>SignerInfo</b> object referenced in the <b>SignedData</b> object contains the signature information. For a more complete discussion, see <a href="/windows/desktop/SecCertEnroll/pkcs--7-attributes">PKCS #7 Attributes</a>.

``` syntax

-------------------------------------------------------------------
-- signed-data
-------------------------------------------------------------------

SignedData ::= SEQUENCE 
{
  version           INTEGER,
  digestAlgorithms  DigestAlgorithmIdentifiers,
  contentInfo       ContentInfo,
  certificates      [0] IMPLICIT Certificates OPTIONAL,
  crls              [1] IMPLICIT CertificateRevocationLists OPTIONAL,
  signerInfos       SignerInfos
}

SignerInfo ::= SEQUENCE 
{
  version                     INTEGER,
  sid                         CertIdentifier,
  digestAlgorithm             DigestAlgorithmIdentifier,
  authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
  signatureAlgorithm          SignatureAlgorithmIdentifier,
  signature                   SignatureValue,
  unauthenticatedAttributes   [1] IMPLICIT Attributes
}
 
```


## -inheritance

The <b>IX509CertificateRequestPkcs7</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>. <b>IX509CertificateRequestPkcs7</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>
