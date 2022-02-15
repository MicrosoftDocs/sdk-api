---
UID: NN:certenroll.IX509CertificateRequestPkcs10
title: IX509CertificateRequestPkcs10 (certenroll.h)
description: The IX509CertificateRequestPkcs10 interface represents a PKCS
helpviewer_keywords: ["IX509CertificateRequestPkcs10","IX509CertificateRequestPkcs10 interface [Security]","IX509CertificateRequestPkcs10 interface [Security]","described","certenroll/IX509CertificateRequestPkcs10","security.ix509certificaterequestpkcs10"]
old-location: security\ix509certificaterequestpkcs10.htm
tech.root: security
ms.assetid: 5b3764dc-fc63-45cc-8c35-65539c461e81
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs10 interface [Security], IX509CertificateRequestPkcs10 interface [Security],described, certenroll/IX509CertificateRequestPkcs10, security.ix509certificaterequestpkcs10
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
 - IX509CertificateRequestPkcs10
 - certenroll/IX509CertificateRequestPkcs10
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
 - IX509CertificateRequestPkcs10
---

# IX509CertificateRequestPkcs10 interface


## -description

The <b>IX509CertificateRequestPkcs10</b> interface represents a PKCS #10 certificate request. The public key cryptography standard (PKCS) #10 defines the format of messages sent to a certification or registration authority to request a public-key certificate.

A PKCS #10 ASN.1 request object contains a version identifier, the subject name, a public key and a set of attributes as shown by the following syntax example.

``` syntax

--------------------------------------------------------------------
-- Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

-------------------------------------------------------
-- Version number.
-------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

-------------------------------------------------------
-- Subject distinguished name (DN).
-------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               EncodedObjectID,
   value              ANY 
}

-------------------------------------------------------
-- Public key information.
-------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

-------------------------------------------------------
-- Attributes.
-------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               EncodedObjectID,
   values             AttributeSetValue
}
```
The <b>CertificationRequestInfo</b> ASN.1 object is wrapped in a <b>CertificationRequest</b> object as shown by the following syntax. The <b>CertificationRequest</b> object also includes the signature and  the signature algorithm. A PKCS #10 request must be signed by the associated private key or null-signed if it is a cross-certification request. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_rawdata">RawData</a> property to retrieve the signed <b>CertificationRequest</b> object, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_rawdatatobesigned">RawDataToBeSigned</a> property to retrieve the unsigned <b>CertificationRequestInfo</b> object.

``` syntax

--------------------------------------------------------------------
-- Certificate request.
--------------------------------------------------------------------
CertificationRequest ::= SEQUENCE 
{
   certificationRequestInfo   CertificationRequestInfo,
   signatureAlgorithm         AlgorithmIdentifier,
   signature                  BIT STRING
}

--------------------------------------------
--  Algorithm Identifier
--------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
   algorithm           EncodedObjectID,
   parameters          ANY OPTIONAL
}

```
The following properties can be set before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_clientid">ClientId</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_hashalgorithm">HashAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_renewalcertificate">RenewalCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_suppressdefaults">SuppressDefaults</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>Also, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>, and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_uicontextmessage">UIContextMessage</a> properties are typically called before calling an initialization method.

The following properties must be set, if at all, before calling the Encode method:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_keycontainernameprefix">KeyContainerNamePrefix</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_subject">Subject</a>
</li>
</ul>

## -inheritance

The <b>IX509CertificateRequestPkcs10</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>. <b>IX509CertificateRequestPkcs10</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>
