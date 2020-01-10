---
UID: NN:certenroll.IX509ExtensionBasicConstraints
title: IX509ExtensionBasicConstraints (certenroll.h)
description: Enables you to specify whether the certificate subject is a certification authority and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined.
old-location: security\ix509extensionbasicconstraints.htm
tech.root: seccertenroll
ms.assetid: 81a1d567-191f-463c-ba67-0867025d8756
ms.date: 12/05/2018
ms.keywords: IX509ExtensionBasicConstraints, IX509ExtensionBasicConstraints interface [Security], IX509ExtensionBasicConstraints interface [Security],described, certenroll/IX509ExtensionBasicConstraints, security.ix509extensionbasicconstraints
f1_keywords:
- certenroll/IX509ExtensionBasicConstraints
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
- IX509ExtensionBasicConstraints
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionBasicConstraints interface


## -description


The <b>IX509ExtensionBasicConstraints</b> interface enables you to specify whether the certificate subject is a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined. This extension must be marked <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> in any certification authority certificate that contains a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a> used to validate a digital signature on a certificate.  The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and is included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- Basic Constraints
-- XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19)
----------------------------------------------------------------------

BasicConstraints2 ::= SEQUENCE 
{
   cA                  BOOLEAN DEFAULT FALSE,
   pathLenConstraint   INTEGER OPTIONAL
}</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionBasicConstraints</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionBasicConstraints</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionBasicConstraints</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a Boolean value that indicates whether the certificate subject is a certification authority (CA) and an integer that contains the depth of the subordinate CA chain.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionBasicConstraints</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-get_isca">IsCA</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-get_pathlenconstraint">PathLenConstraint</a>


</td>
<td align="left" width="63%">
Retrieves the depth of the subordinate certification authority chain.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
 

 

