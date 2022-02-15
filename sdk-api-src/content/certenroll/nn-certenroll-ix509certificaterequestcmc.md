---
UID: NN:certenroll.IX509CertificateRequestCmc
title: IX509CertificateRequestCmc (certenroll.h)
description: Represents a CMC (Certificate Management Message over CMS) certificate request.
helpviewer_keywords: ["IX509CertificateRequestCmc","IX509CertificateRequestCmc interface [Security]","IX509CertificateRequestCmc interface [Security]","described","certenroll/IX509CertificateRequestCmc","security.ix509certificaterequestcmc"]
old-location: security\ix509certificaterequestcmc.htm
tech.root: security
ms.assetid: 77059388-c442-4db5-ab27-1db25e2f63b9
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc, IX509CertificateRequestCmc interface [Security], IX509CertificateRequestCmc interface [Security],described, certenroll/IX509CertificateRequestCmc, security.ix509certificaterequestcmc
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
 - IX509CertificateRequestCmc
 - certenroll/IX509CertificateRequestCmc
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
 - IX509CertificateRequestCmc
---

# IX509CertificateRequestCmc interface


## -description

The <b>IX509CertificateRequestCmc</b> interface represents a CMC (Certificate Management Message over CMS) certificate request.  A CMC request is always wrapped by a PKCS #7 certificate message syntax (CMS) object. Therefore, the <b>IX509CertificateRequestCmc</b> interface inherits from the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> interface.

A CMC request contains sequences of <b>TaggedAttribute</b>, <b>TaggedRequest</b>, and <b>TaggedContentInfo</b> ASN.1 structures. The <b>TaggedOtherMsg</b> structure identified in the RFC is not supported.

``` syntax

CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo
OtherMsgSequence ::=    SEQUENCE OF TaggedOtherMsg

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```
A CMC request can contain a PKCS #10 request in the <b>TaggedRequest</b> sequence or another CMC request object in the <b>TaggedContentInfo</b> sequence. There is no theoretical limit to the possible number of nesting levels, but certification authorities typically place a physical limit on the request size.

The <b>TaggedAttribute</b> sequence contains extensions and optional attributes. For more information, see <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> and <a href="/windows/desktop/SecCertEnroll/cmc-attributes">CMC Attributes</a>.

## -inheritance

The <b>IX509CertificateRequestCmc</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>. <b>IX509CertificateRequestCmc</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
