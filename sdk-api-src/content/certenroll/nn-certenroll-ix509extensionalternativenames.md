---
UID: NN:certenroll.IX509ExtensionAlternativeNames
title: IX509ExtensionAlternativeNames
author: windows-sdk-content
description: Enables you to specify one or more alternative name forms for the subject of a certificate. A certification authority processes the extension by binding the names to the certified public key.
old-location: security\ix509extensionalternativenames.htm
old-project: seccertenroll
ms.assetid: facfcc85-c1ca-47a1-90a6-10522b15cc65
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509ExtensionAlternativeNames, IX509ExtensionAlternativeNames interface [Security], IX509ExtensionAlternativeNames interface [Security],described, certenroll/IX509ExtensionAlternativeNames, security.ix509extensionalternativenames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - IX509ExtensionAlternativeNames
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionAlternativeNames interface


## -description


The <b>IX509ExtensionAlternativeNames</b> interface enables you to specify one or more alternative name forms for the subject of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>. A <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the extension by binding the names to the certified <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- AlternativeNames 
-- XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17)
----------------------------------------------------------------------

AltNames ::= SEQUENCE --#public-- OF GeneralName
GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5STRING,
   dNSName                 [2] IMPLICIT IA5STRING,
   x400Address             [3] IMPLICIT SeqOfAny,       -- Not supported
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SeqOfAny,
   uniformResourceLocator  [6] IMPLICIT IA5STRING,
   iPAddress               [7] IMPLICIT OCTETSTRING,
   registeredID            [8] IMPLICIT EncodedObjectID -- Not supported
}

OtherName ::= SEQUENCE 
{
   type                    EncodedObjectID,
   value                   [0] EXPLICIT NOCOPYANY 
}
</code></pre> If you  initialize this extension by using an <a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a> collection, the following name types are supported.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an object identifier and a byte array that contains the name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a Domain Name System name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> directory name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an Internet Protocol (IP) address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID. This is a form of <b>otherName</b>.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN). The UPN format is based on RFC 822.</td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAlternativeNames</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionAlternativeNames</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionAlternativeNames</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a314dfac-fe17-4e33-b528-491a2622e80c">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e520b2b4-c181-4fb1-98e8-f159bd0d31b4">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from an <a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionAlternativeNames</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/816afa9d-2283-4e17-ad12-ee53e5353d83">AlternativeNames</a>


</td>
<td align="left" width="63%">
Retrieves a collection of subject alternative names.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f2a6854d-1831-489f-adf6-31a0b26511e3">Extensions</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

