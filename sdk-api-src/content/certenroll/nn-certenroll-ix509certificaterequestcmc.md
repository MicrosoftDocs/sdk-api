---
UID: NN:certenroll.IX509CertificateRequestCmc
title: IX509CertificateRequestCmc
author: windows-driver-content
description: Represents a CMC (Certificate Management Message over CMS) certificate request.
old-location: security\ix509certificaterequestcmc.htm
old-project: SecCertEnroll
ms.assetid: 77059388-c442-4db5-ab27-1db25e2f63b9
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateRequestCmc, IX509CertificateRequestCmc interface [Security], IX509CertificateRequestCmc interface [Security],described, certenroll/IX509CertificateRequestCmc, security.ix509certificaterequestcmc
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestCmc
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc interface


## -description


The <b>IX509CertificateRequestCmc</b> interface represents a CMC (Certificate Management Message over CMS) certificate request.  A CMC request is always wrapped by a PKCS #7 certificate message syntax (CMS) object. Therefore, the <b>IX509CertificateRequestCmc</b> interface inherits from the <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> interface.

A CMC request contains sequences of <b>TaggedAttribute</b>, <b>TaggedRequest</b>, and <b>TaggedContentInfo</b> ASN.1 structures. The <b>TaggedOtherMsg</b> structure identified in the RFC is not supported.
<pre class="syntax" xml:space="preserve"><code>
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo
OtherMsgSequence ::=    SEQUENCE OF TaggedOtherMsg

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY</code></pre>A CMC request can contain a PKCS #10 request in the <b>TaggedRequest</b> sequence or another CMC request object in the <b>TaggedContentInfo</b> sequence. There is no theoretical limit to the possible number of nesting levels, but certification authorities typically place a physical limit on the request size.

The <b>TaggedAttribute</b> sequence contains extensions and optional attributes. For more information, see <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> and <a href="https://msdn.microsoft.com/faeee338-bce4-4b35-9be9-72a6568fa259">CMC Attributes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCmc</b> interface inherits from <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>. <b>IX509CertificateRequestCmc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequestCmc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abf7617e-1194-4303-a214-23fbaf20eccf">InitializeFromInnerRequestTemplateName</a>
</td>
<td align="left" width="63%">
Initializes the certificate request from an inner request  object and a template.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCmc</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/06c5d148-eecc-45db-9d82-ec56c226ffed">CriticalExtensions</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/733d29d8-95ea-4193-99b0-a07fcf560435">CryptAttributes</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection of optional certificate attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/63aba8aa-bee7-46b6-a821-4e4d440356ac">EncryptedKeyHash</a>


</td>
<td align="left" width="63%">
Retrieves a hash of the private key to be archived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c46b3373-6d9e-46d9-a36a-b73a718ddaf7">EncryptionAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies or retrieves an object identifier of the algorithm used to encrypt the private key to be archived.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9cade9f0-d614-4838-bf42-0a19b4ce53d5">EncryptionStrength</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the relative encryption level applied to the private key to be archived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93f71fd7-33bb-4352-b184-7270bca1363f">KeyArchivalCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a certification authority (CA) encryption certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3b98629e-a501-4ba0-8825-0cab7187d6f5">NameValuePairs</a>


</td>
<td align="left" width="63%">
Retrieves a collection of name-value pairs that can be associated with a certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/99cefeed-caec-401e-bdcd-d167472b2cbd">NullSigned</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the primary signature  on the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7f7ec18f-7b5b-445e-9033-12d86b3675f1">SenderNonce</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a byte array that contains a nonce.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cd5353b4-b1dd-495f-ae75-c6e14edbb8f9">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the primary signature used to sign the certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0b963fe2-32bd-4f99-9d4f-b17cb2d65909">SignerCertificates</a>


</td>
<td align="left" width="63%">
Retrieves a collection of certificates used to sign the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6e0a8245-1bcc-413a-865a-8a6274dd55f5">SuppressOids</a>


</td>
<td align="left" width="63%">
Retrieves a collection of extension or attribute object identifiers to be suppressed from the certificate during the encoding process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/36a87e0e-d910-45a7-9850-512ff94e78b8">TemplateObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the object identifier of the template used to create the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d47e4b6-47bb-4ec4-8248-f4c859e9b9da">TransactionId</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a transaction identifier that can be used to track a certificate request or response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/75eae625-5c41-4eef-aacd-bd1681286b2b">X509Extensions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the extensions included in the certificate request.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

