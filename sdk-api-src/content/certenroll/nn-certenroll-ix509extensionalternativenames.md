---
UID: NN:certenroll.IX509ExtensionAlternativeNames
title: IX509ExtensionAlternativeNames (certenroll.h)
description: Enables you to specify one or more alternative name forms for the subject of a certificate. A certification authority processes the extension by binding the names to the certified public key.
helpviewer_keywords: ["IX509ExtensionAlternativeNames","IX509ExtensionAlternativeNames interface [Security]","IX509ExtensionAlternativeNames interface [Security]","described","certenroll/IX509ExtensionAlternativeNames","security.ix509extensionalternativenames"]
old-location: security\ix509extensionalternativenames.htm
tech.root: security
ms.assetid: facfcc85-c1ca-47a1-90a6-10522b15cc65
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAlternativeNames, IX509ExtensionAlternativeNames interface [Security], IX509ExtensionAlternativeNames interface [Security],described, certenroll/IX509ExtensionAlternativeNames, security.ix509extensionalternativenames
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
 - IX509ExtensionAlternativeNames
 - certenroll/IX509ExtensionAlternativeNames
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
 - IX509ExtensionAlternativeNames
---

# IX509ExtensionAlternativeNames interface


## -description

The <b>IX509ExtensionAlternativeNames</b> interface enables you to specify one or more alternative name forms for the subject of a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. A <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> processes the extension by binding the names to the certified <a href="/windows/desktop/SecGloss/p-gly">public key</a>. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

``` syntax

----------------------------------------------------------------------
-- AlternativeNames 
-- XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17)
----------------------------------------------------------------------

AltNames ::= SEQUENCE --#public-- OF GeneralName
GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5STRING,
   dNSName                 [2] IMPLICIT IA5STRING,
   x400Address             [3] IMPLICIT SeqOfAny,       -- Not supported
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SeqOfAny,
   uniformResourceLocator  [6] IMPLICIT IA5STRING,
   iPAddress               [7] IMPLICIT OCTETSTRING,
   registeredID            [8] IMPLICIT EncodedObjectID -- Not supported
}

OtherName ::= SEQUENCE 
{
   type                    EncodedObjectID,
   value                   [0] EXPLICIT NOCOPYANY 
}

```
 If you  initialize this extension by using an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> collection, the following name types are supported.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an object identifier and a byte array that contains the name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a Domain Name System name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="/windows/desktop/SecGloss/x-gly">X.500</a> directory name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an Internet Protocol (IP) address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID. This is a form of <b>otherName</b>.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN). The UPN format is based on RFC 822.</td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionAlternativeNames</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionAlternativeNames</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/win32/seccrypto/extensions">Extensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
