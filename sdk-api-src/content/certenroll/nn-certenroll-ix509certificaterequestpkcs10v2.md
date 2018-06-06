---
UID: NN:certenroll.IX509CertificateRequestPkcs10V2
title: IX509CertificateRequestPkcs10V2
author: windows-sdk-content
description: The IX509CertificateRequestPkcs10V2 interface represents a PKCS #10 certificate request. It includes all of the methods defined by the IX509CertificateRequestPkcs10 interface and adds methods that enable initialization from certificate request templates.
old-location: security\ix509certificaterequestpkcs10v2.htm
old-project: SecCertEnroll
ms.assetid: 38177793-c15b-4651-8260-c90a151da83e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestPkcs10V2, IX509CertificateRequestPkcs10V2 interface [Security], IX509CertificateRequestPkcs10V2 interface [Security],described, certenroll/IX509CertificateRequestPkcs10V2, security.ix509certificaterequestpkcs10v2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: CertEnroll.dll
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
 - IX509CertificateRequestPkcs10V2
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10V2 interface


## -description


The <b>IX509CertificateRequestPkcs10V2</b> interface represents a PKCS #10 certificate request. It includes all of the methods defined by the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> interface and adds methods that enable initialization from certificate request templates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestPkcs10V2</b> interface inherits from <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>. <b>IX509CertificateRequestPkcs10V2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequestPkcs10V2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c19d9754-e96d-4093-9095-82fa0a4baf37">InitializeFromPrivateKeyTemplate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object and a certificate template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20e94948-1455-46c4-bc8c-55dfde45818c">InitializeFromPublicKeyTemplate</a>
</td>
<td align="left" width="63%">
Initializes a null-signed certificate request by using an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object and a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/599b4dfc-43a2-4be5-aa23-d3844ae442aa">InitializeFromTemplate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using a template.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestPkcs10V2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6cb17dcc-81bf-4396-a368-c974b8136e64">PolicyServer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate enrollment policy (CEP) server that contains the template used during initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/903288b5-c4fd-4302-8140-be84532217c1">Template</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate request template used during initialization.

</td>
</tr>
</table> 

