---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_Issuer
title: IX509CertificateRequestCertificate::get_Issuer
author: windows-driver-content
description: Specifies or retrieves the name of the certificate issuer.
old-location: security\ix509certificaterequestcertificate_issuer_property.htm
old-project: SecCertEnroll
ms.assetid: cf07a0ed-8657-4044-8dcd-fcd350af20ee
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],Issuer property, IX509CertificateRequestCertificate.Issuer, IX509CertificateRequestCertificate.get_Issuer, IX509CertificateRequestCertificate::Issuer, IX509CertificateRequestCertificate::get_Issuer, IX509CertificateRequestCertificate::put_Issuer, Issuer property [Security], Issuer property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::Issuer, certenroll/IX509CertificateRequestCertificate::get_Issuer, certenroll/IX509CertificateRequestCertificate::put_Issuer, get_Issuer, security.ix509certificaterequestcertificate_issuer_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestCertificate.Issuer
-	IX509CertificateRequestCertificate.get_Issuer
-	IX509CertificateRequestCertificate.put_Issuer
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCertificate::get_Issuer


## -description


The <b>Issuer</b> property specifies or retrieves the name of the certificate issuer.

This property is read/write.


## -parameters


## -remarks



If you do not specify this property before calling <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a>, the property value is set by using the subject of the signing certificate. If no signing certificate was supplied, the property value is set by using the subject of the request object.

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




<a href="https://msdn.microsoft.com/49f176d9-33f6-4bc1-992c-c613279b0969">IX500DistinguishedName</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>
 

 

