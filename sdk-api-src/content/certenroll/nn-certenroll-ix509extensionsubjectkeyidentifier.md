---
UID: NN:certenroll.IX509ExtensionSubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier (certenroll.h)
description: Enables you to specify a SubjectKeyIdentifier extension.
helpviewer_keywords: ["IX509ExtensionSubjectKeyIdentifier","IX509ExtensionSubjectKeyIdentifier interface [Security]","IX509ExtensionSubjectKeyIdentifier interface [Security]","described","certenroll/IX509ExtensionSubjectKeyIdentifier","security.ix509extensionsubjectkeyidentifier"]
old-location: security\ix509extensionsubjectkeyidentifier.htm
tech.root: security
ms.assetid: dcf28967-65e0-4669-b1b1-b3d42f1b3d6b
ms.date: 12/05/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier interface [Security], IX509ExtensionSubjectKeyIdentifier interface [Security],described, certenroll/IX509ExtensionSubjectKeyIdentifier, security.ix509extensionsubjectkeyidentifier
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
 - IX509ExtensionSubjectKeyIdentifier
 - certenroll/IX509ExtensionSubjectKeyIdentifier
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
 - IX509ExtensionSubjectKeyIdentifier
---

# IX509ExtensionSubjectKeyIdentifier interface


## -description

The <b>IX509ExtensionSubjectKeyIdentifier</b> interface enables you to specify a <b>SubjectKeyIdentifier</b> extension. When a subject has multiple signing certificates, this extension can be used to help identify which certificate matches a specific <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) signing certificate. The extension is placed in all certificates. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.

``` syntax

----------------------------------------------------------------------
-- SubjectKeyIdentifier
-- XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14)
----------------------------------------------------------------------

SubjectKeyIdentifier ::= KeyIdentifier

KeyIdentifier ::= OCTETSTRING

```
Typically the  value is a 20-byte SHA-1 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the CA signing certificate. When the CA issues a certificate, it copies the hash value into the <b>SubjectKeyIdentifier</b> extension. To find the end-entity certificate signed by a particular CA certificate, chain building software searches until it matches the <b>keyIdentifier</b> field in the <b>AuthorityKeyIdentifier</b> extension on the  CA signing certificate with a <b>SubjectKeyIdentifier</b> extension value on an issued certificate. For more information, see <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a>.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionSubjectKeyIdentifier</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionSubjectKeyIdentifier</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/win32/seccrypto/extensions">Extensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
