---
UID: NN:certenroll.IX509ExtensionSubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier
author: windows-sdk-content
description: Enables you to specify a SubjectKeyIdentifier extension.
old-location: security\ix509extensionsubjectkeyidentifier.htm
tech.root: SecCertEnroll
ms.assetid: dcf28967-65e0-4669-b1b1-b3d42f1b3d6b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier interface [Security], IX509ExtensionSubjectKeyIdentifier interface [Security],described, certenroll/IX509ExtensionSubjectKeyIdentifier, security.ix509extensionsubjectkeyidentifier
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
 - IX509ExtensionSubjectKeyIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSubjectKeyIdentifier interface


## -description


The <b>IX509ExtensionSubjectKeyIdentifier</b> interface enables you to specify a <b>SubjectKeyIdentifier</b> extension. When a subject has multiple signing certificates, this extension can be used to help identify which certificate matches a specific <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) signing certificate. The extension is placed in all certificates. The following syntax shows the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- SubjectKeyIdentifier
-- XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14)
----------------------------------------------------------------------

SubjectKeyIdentifier ::= KeyIdentifier

KeyIdentifier ::= OCTETSTRING
</code></pre>Typically the  value is a 20-byte SHA-1 hash of the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> contained in the CA signing certificate. When the CA issues a certificate, it copies the hash value into the <b>SubjectKeyIdentifier</b> extension. To find the end-entity certificate signed by a particular CA certificate, chain building software searches until it matches the <b>keyIdentifier</b> field in the <b>AuthorityKeyIdentifier</b> extension on the  CA signing certificate with a <b>SubjectKeyIdentifier</b> extension value on an issued certificate. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionSubjectKeyIdentifier</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>. <b>IX509ExtensionSubjectKeyIdentifier</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionSubjectKeyIdentifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378217(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378220(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a byte array that contains the key identifier.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionSubjectKeyIdentifier</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378236(v=VS.85).aspx">SubjectKeyIdentifier</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the key identifier.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa382409(v=VS.85).aspx">Extensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
 

 

