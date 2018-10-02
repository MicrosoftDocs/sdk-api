---
UID: NN:certenroll.IX509Attribute
title: IX509Attribute
author: windows-sdk-content
description: Can be used to represent an attribute in a PKCS #7, PKCS #10, or CMC certificate request.
old-location: security\ix509attribute.htm
tech.root: SecCertEnroll
ms.assetid: 20965768-2c6b-488a-ab7c-5e0f6f28ac9b
ms.author: windowssdkdev
ms.date: 09/26/2018
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
<a href="https://msdn.microsoft.com/en-us/library/Aa375569(v=VS.85).aspx">Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379079(v=VS.85).aspx">PKCS #7 Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379075(v=VS.85).aspx">PKCS #10 Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa374889(v=VS.85).aspx">CMC Attributes</a>
</li>
</ul>


Attributes are added to a certificate request to provide a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> with additional information that it can use when creating and issuing a certificate. Each attribute is a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure that contains an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and zero or more values as shown by the following syntax.
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>
(XCN_OID_REQUEST_CLIENT_INFO)

</td>
<td>Represents an attribute that can be used to identify the client that generated a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a>
(XCN_OID_RSA_certExtensions)

</td>
<td>Represents an attribute that contains certificate extensions in a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377059(v=VS.85).aspx">IX509AttributeArchiveKey</a>
(XCN_OID_ARCHIVED_KEY_ATTR)

</td>
<td> Represents an attribute that contains an encrypted <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> to be archived by a certification authority.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a>
(XCN_OID_ENCRYPTED_KEY_HASH)

</td>
<td>Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>
(XCN_OID_ENROLLMENT_CSP_PROVIDER)

</td>
<td>Represents an attribute that identifies the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) used by the entity requesting the certificate. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377096(v=VS.85).aspx">IX509AttributeOSVersion</a>
(XCN_OID_OS_VERSION)

</td>
<td>Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa377102(v=VS.85).aspx">IX509AttributeRenewalCertificate</a>
(XCN_OID_RENEWAL_CERTIFICATE)

</td>
<td>Represents an attribute that contains the certificate being renewed.</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Attribute</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509Attribute</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377118(v=VS.85).aspx">Initialize</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377120(v=VS.85).aspx">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves an OID for the attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377122(v=VS.85).aspx">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the attribute value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

