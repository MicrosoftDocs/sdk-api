---
UID: NN:certenroll.IX509ExtensionAlternativeNames
title: IX509ExtensionAlternativeNames (certenroll.h)
description: Enables you to specify one or more alternative name forms for the subject of a certificate. A certification authority processes the extension by binding the names to the certified public key.
helpviewer_keywords: ["IX509ExtensionAlternativeNames","IX509ExtensionAlternativeNames interface [Security]","IX509ExtensionAlternativeNames interface [Security]","described","certenroll/IX509ExtensionAlternativeNames","security.ix509extensionalternativenames"]
old-location: security\ix509extensionalternativenames.htm
tech.root: seccertenroll
ms.assetid: facfcc85-c1ca-47a1-90a6-10522b15cc65
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAlternativeNames, IX509ExtensionAlternativeNames interface [Security], IX509ExtensionAlternativeNames interface [Security],described, certenroll/IX509ExtensionAlternativeNames, security.ix509extensionalternativenames
f1_keywords:
- certenroll/IX509ExtensionAlternativeNames
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509ExtensionAlternativeNames
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionAlternativeNames interface


## -description


The <b>IX509ExtensionAlternativeNames</b> interface enables you to specify one or more alternative name forms for the subject of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>. A <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> processes the extension by binding the names to the certified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a>. The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>.
<pre class="syntax" xml:space="preserve"><code>
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
</code></pre> If you  initialize this extension by using an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> collection, the following name types are supported.<table>
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
<td>The name is an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/x-gly">X.500</a> directory name.</td>
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
<td>The name is a registered <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID. This is a form of <b>otherName</b>.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN). The UPN format is based on RFC 822.</td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAlternativeNames</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionAlternativeNames</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionAlternativeNames</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAlternativeNames</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-get_alternativenames">AlternativeNames</a>


</td>
<td align="left" width="63%">
Retrieves a collection of subject alternative names.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nn-mmcobj-extensions">Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
 

 

