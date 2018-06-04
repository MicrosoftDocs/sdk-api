---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IX509ExtensionTemplateName interface


## -description


The <b>IX509ExtensionTemplateName</b> interface defines methods and properties that can be used to initialize or retrieve a template name extension. This extension can be placed in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> to tell the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> what template to use when issuing or renewing a certificate. The template is identified by name.<div class="alert"><b>Note</b>  The <b>CertificateTemplateName</b> extension is used to identify version 1 templates. To identify a version 2 template, you can use the <b>CertificateTemplate</b> extension defined by the <a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a> interface.</div>
<div> </div>


The extension is encoded as a name-value pair where name equals the Unicode string "CertificateTemplate" and the associated value is the name of the template. The following syntax shows an example of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) output for the template named "User". The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER).
<pre class="syntax" xml:space="preserve"><code>
30 42				; SEQUENCE (42 Bytes)
|  06 0a				; OBJECT_ID (a Bytes)
|  |  2b 06 01 04 01 82 37 0d  02 01
|  |     ; 1.3.6.1.4.1.311.13.2.1 Enrollment Name Value Pair
|  31 34				; SET (34 Bytes)
|     30 32			; SEQUENCE (32 Bytes)
|        1e 26			; UNICODE_STRING (26 Bytes)
|        |  00 43 00 65 00 72 00 74  00 69 00 66 00 69 00 63  ; .C.e.r.t.i.f.i.c
|        |  00 61 00 74 00 65 00 54  00 65 00 6d 00 70 00 6c  ; .a.t.e.T.e.m.p.l
|        |  00 61 00 74 00 65                                 ; .a.t.e
|        |     ; "CertificateTemplate"
|        1e 08			; UNICODE_STRING (8 Bytes)
|           00 55 00 73 00 65 00 72                           ; .U.s.e.r
|              ; "User"
</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplateName</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionTemplateName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionTemplateName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05fb275c-75b2-4619-8d6a-c6c9868d9765">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b72b73a-bfd5-4a56-a106-01f2fd59e922">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a string that contains the template name.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplateName</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b403a27f-e477-4445-adcb-5fce58453727">TemplateName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the template.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

