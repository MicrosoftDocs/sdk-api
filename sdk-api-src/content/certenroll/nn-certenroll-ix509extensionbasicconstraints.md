---
UID: NN:certenroll.IX509ExtensionBasicConstraints
title: IX509ExtensionBasicConstraints
author: windows-sdk-content
description: Enables you to specify whether the certificate subject is a certification authority and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined.
old-location: security\ix509extensionbasicconstraints.htm
old-project: SecCertEnroll
ms.assetid: 81a1d567-191f-463c-ba67-0867025d8756
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509ExtensionBasicConstraints, IX509ExtensionBasicConstraints interface [Security], IX509ExtensionBasicConstraints interface [Security],described, certenroll/IX509ExtensionBasicConstraints, security.ix509extensionbasicconstraints
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionBasicConstraints
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionBasicConstraints interface


## -description


The <b>IX509ExtensionBasicConstraints</b> interface enables you to specify whether the certificate subject is a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> and, if so, the depth of the subordinate certification authority chain that can exist beneath the certification authority for which this extension ID is defined. This extension must be marked <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> in any certification authority certificate that contains a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> used to validate a digital signature on a certificate.  The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and is included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- Basic Constraints
-- XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19)
----------------------------------------------------------------------

BasicConstraints2 ::= SEQUENCE 
{
   cA                  BOOLEAN DEFAULT FALSE,
   pathLenConstraint   INTEGER OPTIONAL
}</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionBasicConstraints</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionBasicConstraints</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3b0b5547-6871-412a-8463-889af3b1302b">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9a08445-8fc5-45cc-a2c6-ec62470e5c55">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/1547d015-b497-4f91-acc2-4cbb2a69709f">IsCA</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6d688596-60fd-47d0-8f91-cfda448ac015">PathLenConstraint</a>


</td>
<td align="left" width="63%">
Retrieves the depth of the subordinate certification authority chain.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

