---
UID: NN:certenroll.IX509CertificateRequestCmc2
title: IX509CertificateRequestCmc2
author: windows-driver-content
description: The IX509CertificateRequestCmc2 interface represents a CMC (Certificate Management Message over CMS) certificate request.
old-location: security\ix509certificaterequestcmc2.htm
old-project: SecCertEnroll
ms.assetid: 27edf846-472e-4a22-bd3c-88044a1fbd99
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509CertificateRequestCmc2, IX509CertificateRequestCmc2 interface [Security], IX509CertificateRequestCmc2 interface [Security],described, certenroll/IX509CertificateRequestCmc2, security.ix509certificaterequestcmc2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestCmc2
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc2 interface


## -description


The <b>IX509CertificateRequestCmc2</b> interface represents a CMC (Certificate Management Message over CMS) certificate request. It includes all of the methods defined by the <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> interface and adds methods that enable initialization from certificate request templates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCmc2</b> interface inherits from <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>. <b>IX509CertificateRequestCmc2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequestCmc2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10ccda23-98d7-49ad-bb0c-60050d01892d">CheckCertificateSignature</a>
</td>
<td align="left" width="63%">
Verifies the signature for a specified signer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55051bcd-0002-4a0e-874e-8b09e196a838">CheckSignature</a>
</td>
<td align="left" width="63%">
Verifies that the certificate request has been signed and that the signature is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12490859-bb4a-49ff-9d92-24bf04ab3999">InitializeFromInnerRequestTemplate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request from an inner request  object and a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/576e3349-1da7-4f1e-9410-a72c30e22063">InitializeFromTemplate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using a template.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCmc2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3a0aa790-c337-4033-a8fa-52f2b06ac005">PolicyServer</a>


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

<a href="https://msdn.microsoft.com/50c1b376-60e4-4a77-8e12-01fd61805d92">Template</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate request template used during initialization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

