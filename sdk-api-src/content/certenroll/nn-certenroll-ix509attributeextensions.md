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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeExtensions interface


## -description


The <b>IX509AttributeExtensions</b> interface defines methods and properties that initialize and retrieve certificate extensions in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. For example, the  <b>CertificateRequestInfo</b> structure of a  PKCS #10 request does not contain a field for version 3 extensions. Instead, the extensions must be added to the attributes collection in the request.
<pre class="syntax" xml:space="preserve"><code>
CertificationRequestInfo ::= SEQUENCE 
{
   version       INTEGER { v1(0) } (v1,...),
   subject       Name,
   subjectPKInfo SubjectPublicKeyInfo{{ PKInfoAlgorithms }},
   attributes    [0] Attributes{{ CRIAttributes }}
}
</code></pre>Also, extensions are included in a CMC request by adding them to the <b>TaggedAttributes</b> structure shown in the following <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) syntax example. For more information, see <a href="https://msdn.microsoft.com/6116e61e-3ec5-4992-90ab-e3c7ced291b6">Attributes</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa382409(v=VS.85).aspx">Extensions</a>.
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
<li>Initialize any of the following <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a> objects:<ul>
<li>
<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d35d155c-fb81-4d7e-b5c9-82ac5af4b79e">IX509ExtensionCertificatePolicies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/35b6449e-5a82-4f47-bdda-5356f44bb1fd">IX509ExtensionMSApplicationPolicies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a>
</li>
</ul>
</li>
<li>Add the extension objects into an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Use the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection to initialize an <b>IX509AttributeExtensions</b> object. </li>
<li>Add the <b>IX509AttributeExtensions</b> object to an <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> collection.</li>
<li>Use the <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> collection to initialize an <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> object.</li>
<li>Initialize a CMC or PKCS #10 request object and retrieve the <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>Add the <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> object to the <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection for the request.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeExtensions</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeExtensions</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/194f8556-9e26-4fae-ac2b-6c3f07cb22c8">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5b6f0b9-ca49-42f2-842c-34c2445c3824">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the object from an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.

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

<a href="https://msdn.microsoft.com/719c4ac5-8d67-4026-9eb6-9682942ad367">X509Extensions</a>


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




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

