---
UID: NN:certenroll.IX509ExtensionSmimeCapabilities
title: IX509ExtensionSmimeCapabilities (certenroll.h)
description: Can be used to report the decryption capabilities of an email recipient to an email sender so that the sender can choose the most secure algorithm supported by both parties.
helpviewer_keywords: ["IX509ExtensionSmimeCapabilities","IX509ExtensionSmimeCapabilities interface [Security]","IX509ExtensionSmimeCapabilities interface [Security]","described","certenroll/IX509ExtensionSmimeCapabilities","security.ix509extensionsmimecapabilities"]
old-location: security\ix509extensionsmimecapabilities.htm
tech.root: security
ms.assetid: 06dca62d-282b-4bdd-bc8d-4d2e6eb226b5
ms.date: 12/05/2018
ms.keywords: IX509ExtensionSmimeCapabilities, IX509ExtensionSmimeCapabilities interface [Security], IX509ExtensionSmimeCapabilities interface [Security],described, certenroll/IX509ExtensionSmimeCapabilities, security.ix509extensionsmimecapabilities
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
 - IX509ExtensionSmimeCapabilities
 - certenroll/IX509ExtensionSmimeCapabilities
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
 - IX509ExtensionSmimeCapabilities
---

# IX509ExtensionSmimeCapabilities interface


## -description

The <b>IX509ExtensionSmimeCapabilities</b> interface can be used to report the decryption capabilities of an email recipient to an email sender so that  the sender can choose the most secure algorithm supported by both parties. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.

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
The extension can be initialized from a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> objects, each of which identifies a symmetric encryption algorithm and optional key length. The following algorithms are supported.<table>
<tr>
<th>OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC(1.3.14.3.2.7)

</td>
<td>Data Encryption Standard (DES) in cipher block chaining (CBC) mode. The key length is 56 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC(1.2.840.113549.3.7)

</td>
<td>Triple DES (3DES) in CBC mode. The key length is 168 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC(1.2.840.113549.3.2)

</td>
<td>RC2 algorithm in CBC mode. The key length is variable from 40 to 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC4(1.2.840.113549.3.4)

</td>
<td>RC4 algorithm. The key length is variable from 40 to 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMS3DESwrap(1.2.840.113549.1.9.16.3.6)

</td>
<td>3DES used for key wrapping. The key length is 168 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMSRC2wrap(1.2.840.113549.1.9.16.3.7)

</td>
<td>RC2 used for key wrapping. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_CBC(2.16.840.1.101.3.4.1.2)

</td>
<td>Advanced Encryption Standard (AES) in CBC mode. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_CBC(2.16.840.1.101.3.4.1.22)

</td>
<td>AES in CBC mode. The key length is 192 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_CBC(2.16.840.1.101.3.4.1.42)

</td>
<td> AES in CBC mode. The key length is 256 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_WRAP(2.16.840.1.101.3.4.1.5)

</td>
<td>AES used for key wrapping. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_WRAP(2.16.840.1.101.3.4.1.25)

</td>
<td>AES used for key wrapping. The key length is 192 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_WRAP(2.16.840.1.101.3.4.1.45)

</td>
<td>AES used for key wrapping. The key length is 256 bits.</td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionSmimeCapabilities</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionSmimeCapabilities</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
