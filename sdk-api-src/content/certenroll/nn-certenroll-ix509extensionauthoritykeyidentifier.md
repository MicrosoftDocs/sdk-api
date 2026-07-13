---
UID: NN:certenroll.IX509ExtensionAuthorityKeyIdentifier
title: IX509ExtensionAuthorityKeyIdentifier (certenroll.h)
description: Enables you to specify an AuthorityKeyIdentifier extension.
helpviewer_keywords: ["IX509ExtensionAuthorityKeyIdentifier","IX509ExtensionAuthorityKeyIdentifier interface [Security]","IX509ExtensionAuthorityKeyIdentifier interface [Security]","described","certenroll/IX509ExtensionAuthorityKeyIdentifier","security.ix509extensionauthoritykeyidentifier"]
old-location: security\ix509extensionauthoritykeyidentifier.htm
tech.root: security
ms.assetid: 68889c3e-25ea-440a-a776-ef3d11dc6b54
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier interface [Security], IX509ExtensionAuthorityKeyIdentifier interface [Security],described, certenroll/IX509ExtensionAuthorityKeyIdentifier, security.ix509extensionauthoritykeyidentifier
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
 - IX509ExtensionAuthorityKeyIdentifier
 - certenroll/IX509ExtensionAuthorityKeyIdentifier
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
 - IX509ExtensionAuthorityKeyIdentifier
---

# IX509ExtensionAuthorityKeyIdentifier interface


## -description

The <b>IX509ExtensionAuthorityKeyIdentifier</b> interface enables you to specify an <b>AuthorityKeyIdentifier</b> extension. When a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) has multiple signing certificates, this extension can be used to help identify which certification authority certificate was used to sign an issued  certificate. The extension is placed in all certificates other than that of the root. It has the following <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) syntax.  The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

``` syntax

----------------------------------------------------------------------
-- AuthorityKeyIdentifier 
-- XCN_OID_AUTHORITY_KEY_IDENTIFIER2 (2.5.29.35)
----------------------------------------------------------------------

AuthorityKeyId2 ::= SEQUENCE 
{
   keyIdentifier             [0] IMPLICIT KeyIdentifier OPTIONAL,
   authorityCertIssuer       [1] IMPLICIT GeneralNames OPTIONAL,
   authorityCertSerialNumber [2] IMPLICIT CertificateSerialNumber OPTIONAL
} 

KeyIdentifier ::= OCTETSTRING

```
 The default certificate request behavior is to populate only the <b>keyIdentifier</b> field. Typically this  value is a 20-byte SHA-1 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the CA signing certificate. When the CA issues a certificate, it copies the hash value into the <b>SubjectKeyIdentifier</b> extension of the issued certificate. Chain building software searches the available CA certificates until it matches the <b>SubjectKeyIdentifier</b> extension value on the issued certificate with the <b>keyIdentifier</b> field in the <b>AuthorityKeyIdentifier</b> extension on the  CA certificate. For more information about the <b>SubjectKeyIdentifier</b> extension, see <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionAuthorityKeyIdentifier</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionAuthorityKeyIdentifier</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/win32/seccrypto/extensions">Extensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>
