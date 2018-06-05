---
UID: NN:certenroll.IX509CertificateRequestCertificate
title: IX509CertificateRequestCertificate
author: windows-sdk-content
description: The IX509CertificateRequestCertificate interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority.
old-location: security\ix509certificaterequestcertificate.htm
old-project: SecCertEnroll
ms.assetid: 7197a225-b2dc-47bb-8843-d3fb4bf95811
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestCertificate, IX509CertificateRequestCertificate interface [Security], IX509CertificateRequestCertificate interface [Security],described, certenroll/IX509CertificateRequestCertificate, security.ix509certificaterequestcertificate
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
-	IX509CertificateRequestCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCertificate interface


## -description


The <b>IX509CertificateRequestCertificate</b> interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority. The following illustration shows the inheritance structure for this object.

<img alt="Inheritance diagram for a self-generated certificate" src="images/X509Inherit_Requestcertificate.png"/>


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCertificate</b> interface inherits from <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>. <b>IX509CertificateRequestCertificate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequestCertificate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7c7becc-667a-4ee2-ae61-0a009d0c87e7">CheckPublicKeySignature</a>
</td>
<td align="left" width="63%">
Verifies the certificate signature by using the public key of the signing certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCertificate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf07a0ed-8657-4044-8dcd-fcd350af20ee">Issuer</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the name of the certificate issuer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a507e06-382f-40e3-8bbd-fcc6a24718db">NotAfter</a>


</td>
<td align="left" width="63%">
Specifies the date and time after which the certificate is no longer valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2568df97-6864-452d-aa18-a5ee47956abd">NotBefore</a>


</td>
<td align="left" width="63%">
Specifies the date and time before which the certificate is not valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ab9d576d-bca2-4388-97ee-9c409c0084c5">SerialNumber</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a string that contains the certificate serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e3a66651-aa0d-4dbb-afb1-f2492e27fec1">SignerCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the  <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object used to sign the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

