---
UID: NN:certenroll.IX509ExtensionAuthorityKeyIdentifier
title: IX509ExtensionAuthorityKeyIdentifier
author: windows-sdk-content
description: Enables you to specify an AuthorityKeyIdentifier extension.
old-location: security\ix509extensionauthoritykeyidentifier.htm
tech.root: SecCertEnroll
ms.assetid: 68889c3e-25ea-440a-a776-ef3d11dc6b54
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionAuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier interface [Security], IX509ExtensionAuthorityKeyIdentifier interface [Security],described, certenroll/IX509ExtensionAuthorityKeyIdentifier, security.ix509extensionauthoritykeyidentifier
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
 - IX509ExtensionAuthorityKeyIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionAuthorityKeyIdentifier interface


## -description


The <b>IX509ExtensionAuthorityKeyIdentifier</b> interface enables you to specify an <b>AuthorityKeyIdentifier</b> extension. When a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) has multiple signing certificates, this extension can be used to help identify which certification authority certificate was used to sign an issued  certificate. The extension is placed in all certificates other than that of the root. It has the following <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) syntax.  The extension value is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) and included in the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- AuthorityKeyIdentifier 
-- XCN_OID_AUTHORITY_KEY_IDENTIFIER2 (2.5.29.35)
----------------------------------------------------------------------

AuthorityKeyId2 ::= SEQUENCE 
{
   keyIdentifier             [0] IMPLICIT KeyIdentifier OPTIONAL,
   authorityCertIssuer       [1] IMPLICIT GeneralNames OPTIONAL,
   authorityCertSerialNumber [2] IMPLICIT CertificateSerialNumber OPTIONAL
} 

KeyIdentifier ::= OCTETSTRING
</code></pre> The default certificate request behavior is to populate only the <b>keyIdentifier</b> field. Typically this  value is a 20-byte SHA-1 hash of the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> contained in the CA signing certificate. When the CA issues a certificate, it copies the hash value into the <b>SubjectKeyIdentifier</b> extension of the issued certificate. Chain building software searches the available CA certificates until it matches the <b>SubjectKeyIdentifier</b> extension value on the issued certificate with the <b>keyIdentifier</b> field in the <b>AuthorityKeyIdentifier</b> extension on the  CA certificate. For more information about the <b>SubjectKeyIdentifier</b> extension, see <a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAuthorityKeyIdentifier</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>. <b>IX509ExtensionAuthorityKeyIdentifier</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionAuthorityKeyIdentifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378101(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378103(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a byte array.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAuthorityKeyIdentifier</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378100(v=VS.85).aspx">AuthorityKeyIdentifier</a>


</td>
<td align="left" width="63%">
Retrieves a byte array  that contains the extension value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa382409(v=VS.85).aspx">Extensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>
 

 

