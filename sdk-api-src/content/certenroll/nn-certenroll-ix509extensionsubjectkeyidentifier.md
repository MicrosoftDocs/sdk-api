---
UID: NN:certenroll.IX509ExtensionSubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier
author: windows-sdk-content
description: Enables you to specify a SubjectKeyIdentifier extension.
old-location: security\ix509extensionsubjectkeyidentifier.htm
old-project: seccertenroll
ms.assetid: dcf28967-65e0-4669-b1b1-b3d42f1b3d6b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier interface [Security], IX509ExtensionSubjectKeyIdentifier interface [Security],described, certenroll/IX509ExtensionSubjectKeyIdentifier, security.ix509extensionsubjectkeyidentifier
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionSubjectKeyIdentifier interface


## -description


The <b>IX509ExtensionSubjectKeyIdentifier</b> interface enables you to specify a <b>SubjectKeyIdentifier</b> extension. When a subject has multiple signing certificates, this extension can be used to help identify which certificate matches a specific <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) signing certificate. The extension is placed in all certificates. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- SubjectKeyIdentifier
-- XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14)
----------------------------------------------------------------------

SubjectKeyIdentifier ::= KeyIdentifier

KeyIdentifier ::= OCTETSTRING
</code></pre>Typically the  value is a 20-byte SHA-1 hash of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> contained in the CA signing certificate. When the CA issues a certificate, it copies the hash value into the <b>SubjectKeyIdentifier</b> extension. To find the end-entity certificate signed by a particular CA certificate, chain building software searches until it matches the <b>keyIdentifier</b> field in the <b>AuthorityKeyIdentifier</b> extension on the  CA signing certificate with a <b>SubjectKeyIdentifier</b> extension value on an issued certificate. For more information, see <a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionSubjectKeyIdentifier</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionSubjectKeyIdentifier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/5886187d-33b1-4151-a01f-de263c41c27b">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0faf3567-3908-473e-9f5c-392991ea668c">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/b055197c-d659-4b92-92b2-b7955beac08a">SubjectKeyIdentifier</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the key identifier.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f2a6854d-1831-489f-adf6-31a0b26511e3">Extensions</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

