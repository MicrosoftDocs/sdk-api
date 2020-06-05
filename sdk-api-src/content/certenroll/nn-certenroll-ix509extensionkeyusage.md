---
UID: NN:certenroll.IX509ExtensionKeyUsage
title: IX509ExtensionKeyUsage (certenroll.h)
description: Can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.helpviewer_keywords: ["IX509ExtensionKeyUsage","IX509ExtensionKeyUsage interface [Security]","IX509ExtensionKeyUsage interface [Security]","described","certenroll/IX509ExtensionKeyUsage","security.ix509extensionkeyusage"]
old-location: security\ix509extensionkeyusage.htm
tech.root: seccertenroll
ms.assetid: 4325e6aa-99bb-4c9a-9b19-c5352ebf27b9
ms.date: 12/05/2018
ms.keywords: IX509ExtensionKeyUsage, IX509ExtensionKeyUsage interface [Security], IX509ExtensionKeyUsage interface [Security],described, certenroll/IX509ExtensionKeyUsage, security.ix509extensionkeyusage
f1_keywords:
- certenroll/IX509ExtensionKeyUsage
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
- IX509ExtensionKeyUsage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionKeyUsage interface


## -description


The <b>IX509ExtensionKeyUsage</b> interface can be used to define restrictions on the operations that can be performed by the public key contained in the certificate. This is the same purpose as that served by the <b>EnhancedKeyUsage</b> extension, but <b>KeyUsage</b> predates that extension and defines a more limited set of restrictions.  The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- KeyUsage
-- XCN_OID_KEY_USAGE (2.5.29.15)
----------------------------------------------------------------------

KeyUsageExtension ::= Bits
</code></pre>The possible restrictions are defined by using a bitwise-<b>OR</b> combination of the values in the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-x509keyusageflags">X509KeyUsageFlags</a> enumeration.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionKeyUsage</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionKeyUsage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionKeyUsage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension by using the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-x509keyusageflags">X509KeyUsageFlags</a> enumeration.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionKeyUsage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-get_keyusage">KeyUsage</a>


</td>
<td align="left" width="63%">
Retrieves the restrictions placed on the public key.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
 

 

