---
UID: NN:certenroll.IX509CertificateRequestCmc
title: IX509CertificateRequestCmc
author: windows-sdk-content
description: Represents a CMC (Certificate Management Message over CMS) certificate request.
old-location: security\ix509certificaterequestcmc.htm
tech.root: SecCertEnroll
ms.assetid: 77059388-c442-4db5-ab27-1db25e2f63b9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestCmc, IX509CertificateRequestCmc interface [Security], IX509CertificateRequestCmc interface [Security],described, certenroll/IX509CertificateRequestCmc, security.ix509certificaterequestcmc
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
 - IX509CertificateRequestCmc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc interface


## -description


The <b>IX509CertificateRequestCmc</b> interface represents a CMC (Certificate Management Message over CMS) certificate request.  A CMC request is always wrapped by a PKCS #7 certificate message syntax (CMS) object. Therefore, the <b>IX509CertificateRequestCmc</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> interface.

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

The <b>TaggedAttribute</b> sequence contains extensions and optional attributes. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa374889(v=VS.85).aspx">CMC Attributes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCmc</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>. <b>IX509CertificateRequestCmc</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377257(v=VS.85).aspx">InitializeFromInnerRequestTemplateName</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377134(v=VS.85).aspx">ArchivePrivateKey</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377135(v=VS.85).aspx">CriticalExtensions</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377231(v=VS.85).aspx">CryptAttributes</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection of optional certificate attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377243(v=VS.85).aspx">EncryptedKeyHash</a>


</td>
<td align="left" width="63%">
Retrieves a hash of the private key to be archived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377244(v=VS.85).aspx">EncryptionAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies or retrieves an object identifier of the algorithm used to encrypt the private key to be archived.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377250(v=VS.85).aspx">EncryptionStrength</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the relative encryption level applied to the private key to be archived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377262(v=VS.85).aspx">KeyArchivalCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a certification authority (CA) encryption certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377278(v=VS.85).aspx">NameValuePairs</a>


</td>
<td align="left" width="63%">
Retrieves a collection of name-value pairs that can be associated with a certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377283(v=VS.85).aspx">NullSigned</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the primary signature  on the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377382(v=VS.85).aspx">SenderNonce</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a byte array that contains a nonce.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377483(v=VS.85).aspx">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object that contains information about the primary signature used to sign the certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377486(v=VS.85).aspx">SignerCertificates</a>


</td>
<td align="left" width="63%">
Retrieves a collection of certificates used to sign the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377491(v=VS.85).aspx">SuppressOids</a>


</td>
<td align="left" width="63%">
Retrieves a collection of extension or attribute object identifiers to be suppressed from the certificate during the encoding process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377492(v=VS.85).aspx">TemplateObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the object identifier of the template used to create the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377497(v=VS.85).aspx">TransactionId</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a transaction identifier that can be used to track a certificate request or response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377500(v=VS.85).aspx">X509Extensions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the extensions included in the certificate request.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
 

 

