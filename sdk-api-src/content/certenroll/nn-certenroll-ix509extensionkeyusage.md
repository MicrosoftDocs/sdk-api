---
UID: NN:certenroll.IX509ExtensionKeyUsage
title: IX509ExtensionKeyUsage
author: windows-driver-content
description: Can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.
old-location: security\ix509extensionkeyusage.htm
old-project: SecCertEnroll
ms.assetid: 4325e6aa-99bb-4c9a-9b19-c5352ebf27b9
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509ExtensionKeyUsage, IX509ExtensionKeyUsage interface [Security], IX509ExtensionKeyUsage interface [Security],described, certenroll/IX509ExtensionKeyUsage, security.ix509extensionkeyusage
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
-	IX509ExtensionKeyUsage
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionKeyUsage interface


## -description


The <b>IX509ExtensionKeyUsage</b> interface can be used to define restrictions on the operations that can be performed by the public key contained in the certificate. This is the same purpose as that served by the <b>EnhancedKeyUsage</b> extension, but <b>KeyUsage</b> predates that extension and defines a more limited set of restrictions.  The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- KeyUsage
-- XCN_OID_KEY_USAGE (2.5.29.15)
----------------------------------------------------------------------

KeyUsageExtension ::= Bits
</code></pre>The possible restrictions are defined by using a bitwise-<b>OR</b> combination of the values in the <a href="https://msdn.microsoft.com/3fcb91a3-ffcd-419f-a686-3fd2d1e795b3">X509KeyUsageFlags</a> enumeration.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionKeyUsage</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionKeyUsage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5e51a148-0a76-4f38-b92f-fd5209e0b497">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4496125-862c-4ef0-93f3-a513eedeacd1">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension by using the <a href="https://msdn.microsoft.com/3fcb91a3-ffcd-419f-a686-3fd2d1e795b3">X509KeyUsageFlags</a> enumeration.

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

<a href="https://msdn.microsoft.com/ddb23d36-342f-4bd1-9936-72b025c4a03b">KeyUsage</a>


</td>
<td align="left" width="63%">
Retrieves the restrictions placed on the public key.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

