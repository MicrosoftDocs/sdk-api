---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_SignerCertificate
title: IX509CertificateRequestCertificate::get_SignerCertificate
author: windows-sdk-content
description: Specifies or retrieves the ISignerCertificate object used to sign the certificate.
old-location: security\ix509certificaterequestcertificate_signercertificate_property.htm
old-project: SecCertEnroll
ms.assetid: e3a66651-aa0d-4dbb-afb1-f2492e27fec1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SignerCertificate property, IX509CertificateRequestCertificate.SignerCertificate, IX509CertificateRequestCertificate.get_SignerCertificate, IX509CertificateRequestCertificate::SignerCertificate, IX509CertificateRequestCertificate::get_SignerCertificate, IX509CertificateRequestCertificate::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SignerCertificate, certenroll/IX509CertificateRequestCertificate::get_SignerCertificate, certenroll/IX509CertificateRequestCertificate::put_SignerCertificate, get_SignerCertificate, security.ix509certificaterequestcertificate_signercertificate_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
-	IX509CertificateRequestCertificate.SignerCertificate
-	IX509CertificateRequestCertificate.get_SignerCertificate
-	IX509CertificateRequestCertificate.put_SignerCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCertificate::get_SignerCertificate


## -description


The <b>SignerCertificate</b> property specifies or retrieves the  <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object used to sign the certificate.

This property is read/write.


## -parameters


## -remarks



You can set this property if you are not creating a self-signed certificate. If you do not specify the  property value before calling  <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a>, the private key associated with the <a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a> object is used to sign the certificate, and the name of the issuer is set, by default, to the subject name.

You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>
 

 

