---
UID: NN:certenroll.IX509AttributeExtensions
title: IX509AttributeExtensions
author: windows-sdk-content
description: Defines methods and properties that initialize and retrieve certificate extensions in a certificate request.
old-location: security\ix509attributeextensions.htm
tech.root: SecCertEnroll
ms.assetid: d216bcfd-50be-4445-87a5-d1cb223aa70c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509AttributeExtensions, IX509AttributeExtensions interface [Security], IX509AttributeExtensions interface [Security],described, certenroll/IX509AttributeExtensions, security.ix509attributeextensions
ms.prod: windows-hardware
ms.technology: windows-devices
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


The <b>IX509AttributeExtensions</b> interface defines methods and properties that initialize and retrieve certificate extensions in a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>. For example, the  <b>CertificateRequestInfo</b> structure of a  PKCS #10 request does not contain a field for version 3 extensions. Instead, the extensions must be added to the attributes collection in the request.
<pre class="syntax" xml:space="preserve"><code>
CertificationRequestInfo ::= SEQUENCE 
{
   version       INTEGER { v1(0) } (v1,...),
   subject       Name,
   subjectPKInfo SubjectPublicKeyInfo{{ PKInfoAlgorithms }},
   attributes    [0] Attributes{{ CRIAttributes }}
}
</code></pre>Also, extensions are included in a CMC request by adding them to the <b>TaggedAttributes</b> structure shown in the following <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) syntax example. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa375569(v=VS.85).aspx">Attributes</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa382409(v=VS.85).aspx">Extensions</a>.
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
<li>Initialize any of the following <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a> objects:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378155(v=VS.85).aspx">IX509ExtensionMSApplicationPolicies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378132(v=VS.85).aspx">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a>
</li>
</ul>
</li>
<li>Add the extension objects into an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection to initialize an <b>IX509AttributeExtensions</b> object. </li>
<li>Add the <b>IX509AttributeExtensions</b> object to an <a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a> collection.</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a> collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a> object.</li>
<li>Initialize a CMC or PKCS #10 request object and retrieve the <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection.</li>
<li>Add the <a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a> object to the <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection for the request.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeExtensions</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>. <b>IX509AttributeExtensions</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377091(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377092(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the object from an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.

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

<a href="https://msdn.microsoft.com/en-us/library/Aa377095(v=VS.85).aspx">X509Extensions</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

