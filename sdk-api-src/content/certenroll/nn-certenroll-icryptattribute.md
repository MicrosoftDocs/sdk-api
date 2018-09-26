---
UID: NN:certenroll.ICryptAttribute
title: ICryptAttribute
author: windows-sdk-content
description: The ICryptAttribute interface represents a cryptographic attribute in a certificate request. A collection of these attributes is contained in the CertificateRequestInfo structure of a PKCS #10 request as shown by the following example syntax.
old-location: security\icryptattribute.htm
tech.root: seccertenroll
ms.assetid: 2aefde1b-0f77-4a88-8851-5bacd363900b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICryptAttribute, ICryptAttribute interface [Security], ICryptAttribute interface [Security],described, certenroll/ICryptAttribute, security.icryptattribute
ms.prod: windows
ms.technology: windows-sdk
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
 - ICryptAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICryptAttribute interface


## -description


The <b>ICryptAttribute</b> interface represents a cryptographic attribute in a certificate request. A collection of these attributes is contained in the  <b>CertificateRequestInfo</b> structure of a  PKCS #10 request as shown by the following example syntax.
<pre class="syntax" xml:space="preserve"><code>
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY, 
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
</code></pre>A single <b>ICryptAttribute</b> object corresponds to the attributes collection in the request. The <b>ICryptAttribute</b> object in turn contains a collection of <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a> objects. Each attribute in this collection contains an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> and one or more values. Each value is an encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure. Zero or more of the following objects can be included in the collection:<ul>
<li>
<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ae84d47-2bda-4954-9165-902634d09da9">IX509AttributeOSVersion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab">IX509AttributeRenewalCertificate</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICryptAttribute</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICryptAttribute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICryptAttribute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6825cca7-c3a5-46a8-9be5-851344629929">InitializeFromObjectId</a>
</td>
<td align="left" width="63%">
Initializes a cryptographic attribute by using an object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/763fd244-173d-4b0b-8809-e98c18b8e5b5">InitializeFromValues</a>
</td>
<td align="left" width="63%">
Initializes a cryptographic attribute by using an <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICryptAttribute</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9ae9a217-1658-42ac-bd28-33abab5d0d70">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the object identifier for the attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ae439c12-65f4-4e2b-b141-6e6bf6738a68">Values</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> object that contains a collection of attributes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

