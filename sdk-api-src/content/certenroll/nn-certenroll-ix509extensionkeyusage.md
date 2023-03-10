---
UID: NN:certenroll.IX509ExtensionKeyUsage
title: IX509ExtensionKeyUsage (certenroll.h)
description: Can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.
helpviewer_keywords: ["IX509ExtensionKeyUsage","IX509ExtensionKeyUsage interface [Security]","IX509ExtensionKeyUsage interface [Security]","described","certenroll/IX509ExtensionKeyUsage","security.ix509extensionkeyusage"]
old-location: security\ix509extensionkeyusage.htm
tech.root: security
ms.assetid: 4325e6aa-99bb-4c9a-9b19-c5352ebf27b9
ms.date: 12/05/2018
ms.keywords: IX509ExtensionKeyUsage, IX509ExtensionKeyUsage interface [Security], IX509ExtensionKeyUsage interface [Security],described, certenroll/IX509ExtensionKeyUsage, security.ix509extensionkeyusage
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
 - IX509ExtensionKeyUsage
 - certenroll/IX509ExtensionKeyUsage
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
 - IX509ExtensionKeyUsage
---

# IX509ExtensionKeyUsage interface


## -description

The <b>IX509ExtensionKeyUsage</b> interface can be used to define restrictions on the operations that can be performed by the public key contained in the certificate. This is the same purpose as that served by the <b>EnhancedKeyUsage</b> extension, but <b>KeyUsage</b> predates that extension and defines a more limited set of restrictions.  The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.

``` syntax

----------------------------------------------------------------------
-- KeyUsage
-- XCN_OID_KEY_USAGE (2.5.29.15)
----------------------------------------------------------------------

KeyUsageExtension ::= Bits

```
The possible restrictions are defined by using a bitwise-<b>OR</b> combination of the values in the <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyusageflags">X509KeyUsageFlags</a> enumeration.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionKeyUsage</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionKeyUsage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
