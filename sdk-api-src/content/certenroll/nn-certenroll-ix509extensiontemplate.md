---
UID: NN:certenroll.IX509ExtensionTemplate
title: IX509ExtensionTemplate (certenroll.h)
author: windows-sdk-content
description: Defines methods and properties that can be used to initialize or retrieve a CertificateTemplate extension.
old-location: security\ix509extensiontemplate.htm
tech.root: seccertenroll
ms.assetid: 2ac24ee9-f31f-4501-a4f0-321580ec2fa9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate, IX509ExtensionTemplate interface [Security], IX509ExtensionTemplate interface [Security],described, certenroll/IX509ExtensionTemplate, security.ix509extensiontemplate
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
ms.custom: 19H1
---

# IX509ExtensionTemplate interface


## -description


The <b>IX509ExtensionTemplate</b> interface defines methods and properties that can be used to initialize or retrieve a <b>CertificateTemplate</b> extension. This extension can be placed in the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a> to tell the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> what template to use when issuing or renewing a certificate. <div class="alert"><b>Note</b>  The <b>CertificateTemplate</b> extension is used to identify version 2 templates. To identify a version 1 template, you can use the <b>CertificateTemplateName</b> extension defined by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a> interface.</div>
<div> </div>The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.
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
</code></pre>To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionTemplate</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionTemplate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a template <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and from major and minor version numbers.

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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_majorversion">MajorVersion</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_minorversion">MinorVersion</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_templateoid">TemplateOid</a>


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




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
 

 

