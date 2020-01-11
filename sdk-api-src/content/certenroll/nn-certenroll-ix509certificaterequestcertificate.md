---
UID: NN:certenroll.IX509CertificateRequestCertificate
title: IX509CertificateRequestCertificate (certenroll.h)
description: The IX509CertificateRequestCertificate interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority.
old-location: security\ix509certificaterequestcertificate.htm
tech.root: seccertenroll
ms.assetid: 7197a225-b2dc-47bb-8843-d3fb4bf95811
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate, IX509CertificateRequestCertificate interface [Security], IX509CertificateRequestCertificate interface [Security],described, certenroll/IX509CertificateRequestCertificate, security.ix509certificaterequestcertificate
f1_keywords:
- certenroll/IX509CertificateRequestCertificate
dev_langs:
- c++
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
- IX509CertificateRequestCertificate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestCertificate interface


## -description


The <b>IX509CertificateRequestCertificate</b> interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority. The following illustration shows the inheritance structure for this object.

<img alt="Inheritance diagram for a self-generated certificate" src="./images/X509Inherit_Requestcertificate.png"/>


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestCertificate</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>. <b>IX509CertificateRequestCertificate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-checkpublickeysignature">CheckPublicKeySignature</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-get_issuer">Issuer</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the name of the certificate issuer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-get_notafter">NotAfter</a>


</td>
<td align="left" width="63%">
Specifies the date and time after which the certificate is no longer valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-get_notbefore">NotBefore</a>


</td>
<td align="left" width="63%">
Specifies the date and time before which the certificate is not valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-get_serialnumber">SerialNumber</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a string that contains the certificate serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate">SignerCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object used to sign the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
 

 

