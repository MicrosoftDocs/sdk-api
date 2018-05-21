---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_X509Extensions
title: IX509CertificateRequestPkcs10::get_X509Extensions
author: windows-driver-content
description: Retrieves a collection of the extensions included in the certificate request.
old-location: security\ix509certificaterequestpkcs10_x509extensions_property.htm
old-project: SecCertEnroll
ms.assetid: b5500c94-7d7a-473d-80ef-c0d713dcb52e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],X509Extensions property, IX509CertificateRequestPkcs10.X509Extensions, IX509CertificateRequestPkcs10.get_X509Extensions, IX509CertificateRequestPkcs10::X509Extensions, IX509CertificateRequestPkcs10::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::X509Extensions, certenroll/IX509CertificateRequestPkcs10::get_X509Extensions, get_X509Extensions, security.ix509certificaterequestpkcs10_x509extensions_property
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
-	IX509CertificateRequestPkcs10.X509Extensions
-	IX509CertificateRequestPkcs10.get_X509Extensions
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_X509Extensions


## -description


The <b>X509Extensions</b> property retrieves a collection of the extensions included in the certificate request. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

