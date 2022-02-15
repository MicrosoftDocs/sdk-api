---
UID: NN:certenroll.IX509ExtensionBasicConstraints
title: IX509ExtensionBasicConstraints (certenroll.h)
description: Enables you to specify whether the certificate subject is a certification authority and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined.
helpviewer_keywords: ["IX509ExtensionBasicConstraints","IX509ExtensionBasicConstraints interface [Security]","IX509ExtensionBasicConstraints interface [Security]","described","certenroll/IX509ExtensionBasicConstraints","security.ix509extensionbasicconstraints"]
old-location: security\ix509extensionbasicconstraints.htm
tech.root: security
ms.assetid: 81a1d567-191f-463c-ba67-0867025d8756
ms.date: 12/05/2018
ms.keywords: IX509ExtensionBasicConstraints, IX509ExtensionBasicConstraints interface [Security], IX509ExtensionBasicConstraints interface [Security],described, certenroll/IX509ExtensionBasicConstraints, security.ix509extensionbasicconstraints
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
 - IX509ExtensionBasicConstraints
 - certenroll/IX509ExtensionBasicConstraints
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
 - IX509ExtensionBasicConstraints
---

# IX509ExtensionBasicConstraints interface


## -description

The <b>IX509ExtensionBasicConstraints</b> interface enables you to specify whether the certificate subject is a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined. This extension must be marked <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> in any certification authority certificate that contains a <a href="/windows/desktop/SecGloss/p-gly">public key</a> used to validate a digital signature on a certificate.  The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and is included in the certificate request.

``` syntax

----------------------------------------------------------------------
-- Basic Constraints
-- XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19)
----------------------------------------------------------------------

BasicConstraints2 ::= SEQUENCE 
{
   cA                  BOOLEAN DEFAULT FALSE,
   pathLenConstraint   INTEGER OPTIONAL
}
```
To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionBasicConstraints</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionBasicConstraints</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
