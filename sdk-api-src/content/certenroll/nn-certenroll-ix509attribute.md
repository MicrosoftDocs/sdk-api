---
UID: NN:certenroll.IX509Attribute
title: IX509Attribute (certenroll.h)
description: Can be used to represent an attribute in a PKCS
old-location: security\ix509attribute.htm
tech.root: seccertenroll
ms.assetid: 20965768-2c6b-488a-ab7c-5e0f6f28ac9b
ms.date: 12/05/2018
ms.keywords: IX509Attribute, IX509Attribute interface [Security], IX509Attribute interface [Security],described, certenroll/IX509Attribute, security.ix509attribute
f1_keywords:
- certenroll/IX509Attribute
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
- IX509Attribute
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509Attribute interface


## -description


The <b>IX509Attribute</b> interface can be used to represent an attribute in a PKCS #7, PKCS #10, or CMC certificate request. For more information, see the following topics:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/attributes">Attributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--7-attributes">PKCS #7 Attributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--10-attributes">PKCS #10 Attributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/cmc-attributes">CMC Attributes</a>
</li>
</ul>


Attributes are added to a certificate request to provide a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> with additional information that it can use when creating and issuing a certificate. Each attribute is a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure that contains an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and zero or more values as shown by the following syntax.
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>
(XCN_OID_REQUEST_CLIENT_INFO)

</td>
<td>Represents an attribute that can be used to identify the client that generated a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>
(XCN_OID_RSA_certExtensions)

</td>
<td>Represents an attribute that contains certificate extensions in a certificate request.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
(XCN_OID_ARCHIVED_KEY_ATTR)

</td>
<td> Represents an attribute that contains an encrypted <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> to be archived by a certification authority.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a>
(XCN_OID_ENCRYPTED_KEY_HASH)

</td>
<td>Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority. </td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>
(XCN_OID_ENROLLMENT_CSP_PROVIDER)

</td>
<td>Represents an attribute that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) used by the entity requesting the certificate. </td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>
(XCN_OID_OS_VERSION)

</td>
<td>Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributerenewalcertificate">IX509AttributeRenewalCertificate</a>
(XCN_OID_RENEWAL_CERTIFICATE)

</td>
<td>Represents an attribute that contains the certificate being renewed.</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Attribute</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509Attribute</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attribute-initialize">Initialize</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attribute-get_objectid">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves an OID for the attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attribute-get_rawdata">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the attribute value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

