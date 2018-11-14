---
UID: NN:certenroll.IX509ExtensionTemplate
title: IX509ExtensionTemplate
author: windows-sdk-content
description: Defines methods and properties that can be used to initialize or retrieve a CertificateTemplate extension.
old-location: security\ix509extensiontemplate.htm
tech.root: SecCertEnroll
ms.assetid: 2ac24ee9-f31f-4501-a4f0-321580ec2fa9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionTemplate, IX509ExtensionTemplate interface [Security], IX509ExtensionTemplate interface [Security],described, certenroll/IX509ExtensionTemplate, security.ix509extensiontemplate
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
 - IX509ExtensionTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplate interface


## -description


The <b>IX509ExtensionTemplate</b> interface defines methods and properties that can be used to initialize or retrieve a <b>CertificateTemplate</b> extension. This extension can be placed in the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> to tell the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> what template to use when issuing or renewing a certificate. <div class="alert"><b>Note</b>  The <b>CertificateTemplate</b> extension is used to identify version 2 templates. To identify a version 1 template, you can use the <b>CertificateTemplateName</b> extension defined by the <a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a> interface.</div>
<div> </div>The following syntax shows the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- CertificateTemplate
-- XCN_OID_CERTIFICATE_TEMPLATE (1.3.6.1.4.1.311.21.7)
----------------------------------------------------------------------

CertificateTemplate ::= SEQUENCE 
{
   templateID              EncodedObjectID,
   templateMajorVersion    TemplateVersion,
   templateMinorVersion    TemplateVersion OPTIONAL
}

TemplateVersion ::= INTEGER (0..4294967295)
</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplate</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>. <b>IX509ExtensionTemplate</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionTemplate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378307(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378310(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a template <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and from major and minor version numbers.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378314(v=VS.85).aspx">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum major version number of the certificate template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum minor version number of the certificate template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378403(v=VS.85).aspx">TemplateOid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the template OID.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
 

 

