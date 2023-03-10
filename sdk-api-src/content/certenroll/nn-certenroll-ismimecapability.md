---
UID: NN:certenroll.ISmimeCapability
title: ISmimeCapability (certenroll.h)
description: Represents an SMIMECapabilities extension that identifies the decryption capabilities of an email recipient.
helpviewer_keywords: ["ISmimeCapability","ISmimeCapability interface [Security]","ISmimeCapability interface [Security]","described","certenroll/ISmimeCapability","security.ismimecapability"]
old-location: security\ismimecapability.htm
tech.root: security
ms.assetid: 3cfbb16f-88fa-41f1-b719-cd5e8ad636cc
ms.date: 12/05/2018
ms.keywords: ISmimeCapability, ISmimeCapability interface [Security], ISmimeCapability interface [Security],described, certenroll/ISmimeCapability, security.ismimecapability
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
 - ISmimeCapability
 - certenroll/ISmimeCapability
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
 - ISmimeCapability
---

# ISmimeCapability interface


## -description

A collection of <b>ISmimeCapability</b> objects represents an <b>SMIMECapabilities</b> extension that identifies the  decryption capabilities of an email recipient. The extension includes a collection of <b>ISmimeCapability</b> objects, each of which identifies a symmetric encryption algorithm supported by the client, and an optional bit length that indicates the relative strength of the algorithm. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension is represented by an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a> interface.

``` syntax

----------------------------------------------------------------------
-- SMIMECapabilities
-- XCN_OID_RSA_SMIMECapabilities (1.2.840.113549.1.9.15)
----------------------------------------------------------------------

SMIMECapabilities ::= SEQUENCE OF SMIMECapability

SMIMECapability ::= SEQUENCE 
{
   capabilityID    EncodedObjectID,
   smimeParameters ANY OPTIONAL    
}

```
The extension is used to report the decryption capabilities of an email recipient to an email sender. This enables the sender to choose the most secure algorithm supported by both parties.

The optional bit length is used to identify the length of the encryption key used by algorithm. The key length is implicitly defined by the object identifier for the AES, DES, and 3DES algorithms, but it is variable for the RC2 and RC4 algorithms. If you specify a key length, it must be consistent with that supported by the cryptographic  providers used by the client. For more information, see <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>.

## -inheritance

The <b>ISmimeCapability</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISmimeCapability</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
