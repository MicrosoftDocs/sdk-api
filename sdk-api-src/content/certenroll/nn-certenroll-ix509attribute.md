---
UID: NN:certenroll.IX509Attribute
title: IX509Attribute
author: windows-sdk-content
description: Can be used to represent an attribute in a PKCS #7, PKCS #10, or CMC certificate request.
old-location: security\ix509attribute.htm
tech.root: seccertenroll
ms.assetid: 20965768-2c6b-488a-ab7c-5e0f6f28ac9b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509Attribute, IX509Attribute interface [Security], IX509Attribute interface [Security],described, certenroll/IX509Attribute, security.ix509attribute
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
 - IX509Attribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Attribute interface


## -description


The <b>IX509Attribute</b> interface can be used to represent an attribute in a PKCS #7, PKCS #10, or CMC certificate request. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/6116e61e-3ec5-4992-90ab-e3c7ced291b6">Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd4e2a13-f257-4ba9-a11d-35f49c5a6c00">PKCS #7 Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f00f638-9edb-474b-a7e4-f6f7b62c89a4">PKCS #10 Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/faeee338-bce4-4b35-9be9-72a6568fa259">CMC Attributes</a>
</li>
</ul>


Attributes are added to a certificate request to provide a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> with additional information that it can use when creating and issuing a certificate. Each attribute is a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure that contains an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and zero or more values as shown by the following syntax.
<pre class="syntax" xml:space="preserve"><code>
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}</code></pre>The <b>IX509Attribute</b> interface can be used to initialize and retrieve an attribute value. It also serves as the base for the following common attribute interfaces.<table>
<tr>
<th>Interface/OID</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>
(XCN_OID_REQUEST_CLIENT_INFO)

</td>
<td>Represents an attribute that can be used to identify the client that generated a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a>
(XCN_OID_RSA_certExtensions)

</td>
<td>Represents an attribute that contains certificate extensions in a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
(XCN_OID_ARCHIVED_KEY_ATTR)

</td>
<td> Represents an attribute that contains an encrypted <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> to be archived by a certification authority.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a>
(XCN_OID_ENCRYPTED_KEY_HASH)

</td>
<td>Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
(XCN_OID_ENROLLMENT_CSP_PROVIDER)

</td>
<td>Represents an attribute that identifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) used by the entity requesting the certificate. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2ae84d47-2bda-4954-9165-902634d09da9">IX509AttributeOSVersion</a>
(XCN_OID_OS_VERSION)

</td>
<td>Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab">IX509AttributeRenewalCertificate</a>
(XCN_OID_RENEWAL_CERTIFICATE)

</td>
<td>Represents an attribute that contains the certificate being renewed.</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Attribute</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509Attribute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509Attribute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82457ca3-4aae-4f47-950c-1146c8614a5b">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from  an OID and a value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Attribute</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a65c7989-5e6e-4253-8ddc-1d1207fecaf8">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves an OID for the attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a8e67f3c-4c05-4742-8251-a03335054b2e">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the attribute value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

