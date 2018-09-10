---
UID: NN:certenroll.IX509ExtensionSmimeCapabilities
title: IX509ExtensionSmimeCapabilities
author: windows-sdk-content
description: Can be used to report the decryption capabilities of an email recipient to an email sender so that the sender can choose the most secure algorithm supported by both parties.
old-location: security\ix509extensionsmimecapabilities.htm
tech.root: SecCertEnroll
ms.assetid: 06dca62d-282b-4bdd-bc8d-4d2e6eb226b5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509ExtensionSmimeCapabilities, IX509ExtensionSmimeCapabilities interface [Security], IX509ExtensionSmimeCapabilities interface [Security],described, certenroll/IX509ExtensionSmimeCapabilities, security.ix509extensionsmimecapabilities
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
 - IX509ExtensionSmimeCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSmimeCapabilities interface


## -description


The <b>IX509ExtensionSmimeCapabilities</b> interface can be used to report the decryption capabilities of an email recipient to an email sender so that  the sender can choose the most secure algorithm supported by both parties. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- SMIMECapabilities
-- XCN_OID_RSA_SMIMECapabilities (1.2.840.113549.1.9.15)
----------------------------------------------------------------------

SMIMECapabilities ::= SEQUENCE OF SMIMECapability

SMIMECapability ::= SEQUENCE 
{
   capabilityID    EncodedObjectID,
   smimeParameters ANY OPTIONAL    
}
</code></pre>The extension can be initialized from a collection of <a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a> objects, each of which identifies a symmetric encryption algorithm and optional key length. The following algorithms are supported.<table>
<tr>
<th>OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC(1.3.14.3.2.7)

</td>
<td>Data Encryption Standard (DES) in cipher block chaining (CBC) mode. The key length is 56 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC(1.2.840.113549.3.7)

</td>
<td>Triple DES (3DES) in CBC mode. The key length is 168 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC(1.2.840.113549.3.2)

</td>
<td>RC2 algorithm in CBC mode. The key length is variable from 40 to 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC4(1.2.840.113549.3.4)

</td>
<td>RC4 algorithm. The key length is variable from 40 to 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMS3DESwrap(1.2.840.113549.1.9.16.3.6)

</td>
<td>3DES used for key wrapping. The key length is 168 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMSRC2wrap(1.2.840.113549.1.9.16.3.7)

</td>
<td>RC2 used for key wrapping. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_CBC(2.16.840.1.101.3.4.1.2)

</td>
<td>Advanced Encryption Standard (AES) in CBC mode. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_CBC(2.16.840.1.101.3.4.1.22)

</td>
<td>AES in CBC mode. The key length is 192 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_CBC(2.16.840.1.101.3.4.1.42)

</td>
<td> AES in CBC mode. The key length is 256 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_WRAP(2.16.840.1.101.3.4.1.5)

</td>
<td>AES used for key wrapping. The key length is 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_WRAP(2.16.840.1.101.3.4.1.25)

</td>
<td>AES used for key wrapping. The key length is 192 bits.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_WRAP(2.16.840.1.101.3.4.1.45)

</td>
<td>AES used for key wrapping. The key length is 256 bits.</td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionSmimeCapabilities</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionSmimeCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionSmimeCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b89b9aa-3e71-4511-8e5a-1fe2165fa672">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/731e3c93-699b-4a99-8520-294f3134aa66">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from an <a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionSmimeCapabilities</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6e3ce718-16f9-47df-aff9-38e922fe505c">SmimeCapabilities</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a> objects.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

