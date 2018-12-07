---
UID: NN:certenroll.IX509ExtensionTemplateName
title: IX509ExtensionTemplateName
author: windows-sdk-content
description: Defines methods and properties that can be used to initialize or retrieve a template name extension.
old-location: security\ix509extensiontemplatename.htm
tech.root: seccertenroll
ms.assetid: 9a2d0219-6fe3-4a75-8d28-281c0b863a35
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509ExtensionTemplateName, IX509ExtensionTemplateName interface [Security], IX509ExtensionTemplateName interface [Security],described, certenroll/IX509ExtensionTemplateName, security.ix509extensiontemplatename
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
 - IX509ExtensionTemplateName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplateName interface


## -description


The <b>IX509ExtensionTemplateName</b> interface defines methods and properties that can be used to initialize or retrieve a template name extension. This extension can be placed in the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> to tell the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> what template to use when issuing or renewing a certificate. The template is identified by name.<div class="alert"><b>Note</b>  The <b>CertificateTemplateName</b> extension is used to identify version 1 templates. To identify a version 2 template, you can use the <b>CertificateTemplate</b> extension defined by the <a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a> interface.</div>
<div> </div>


The extension is encoded as a name-value pair where name equals the Unicode string "CertificateTemplate" and the associated value is the name of the template. The following syntax shows an example of the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) output for the template named "User". The extension value is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER).
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
</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplateName</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>. <b>IX509ExtensionTemplateName</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa378278(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378285(v=VS.85).aspx">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa378302(v=VS.85).aspx">TemplateName</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
 

 

