---
UID: NN:certenroll.IX509AttributeExtensions
title: IX509AttributeExtensions (certenroll.h)
author: windows-sdk-content
description: Defines methods and properties that initialize and retrieve certificate extensions in a certificate request.
old-location: security\ix509attributeextensions.htm
tech.root: seccertenroll
ms.assetid: d216bcfd-50be-4445-87a5-d1cb223aa70c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeExtensions, IX509AttributeExtensions interface [Security], IX509AttributeExtensions interface [Security],described, certenroll/IX509AttributeExtensions, security.ix509attributeextensions
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509AttributeExtensions"
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
 - IX509AttributeExtensions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeExtensions interface


## -description


The <b>IX509AttributeExtensions</b> interface defines methods and properties that initialize and retrieve certificate extensions in a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>. For example, the  <b>CertificateRequestInfo</b> structure of a  PKCS #10 request does not contain a field for version 3 extensions. Instead, the extensions must be added to the attributes collection in the request.
<pre class="syntax" xml:space="preserve"><code>
CertificationRequestInfo ::= SEQUENCE 
{
   version       INTEGER { v1(0) } (v1,...),
   subject       Name,
   subjectPKInfo SubjectPublicKeyInfo{{ PKInfoAlgorithms }},
   attributes    [0] Attributes{{ CRIAttributes }}
}
</code></pre>Also, extensions are included in a CMC request by adding them to the <b>TaggedAttributes</b> structure shown in the following <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) syntax example. For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/attributes">Attributes</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nn-mmcobj-extensions">Extensions</a>.
<pre class="syntax" xml:space="preserve"><code>
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY</code></pre>You can create one or more  version 3 extensions and include them in a certificate request in the following manner:<ul>
<li>Initialize any of the following <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> objects:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>
</li>
</ul>
</li>
<li>Add the extension objects into an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Use the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection to initialize an <b>IX509AttributeExtensions</b> object. </li>
<li>Add the <b>IX509AttributeExtensions</b> object to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a> collection.</li>
<li>Use the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a> collection to initialize an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a> object.</li>
<li>Initialize a CMC or PKCS #10 request object and retrieve the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>Add the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a> object to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection for the request.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeExtensions</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeExtensions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeExtensions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the object from an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeExtensions</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-get_x509extensions">X509Extensions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate extensions.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

