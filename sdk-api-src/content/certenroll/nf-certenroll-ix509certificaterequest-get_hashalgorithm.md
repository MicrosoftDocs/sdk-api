---
UID: NF:certenroll.IX509CertificateRequest.get_HashAlgorithm
title: IX509CertificateRequest::get_HashAlgorithm method
author: windows-driver-content
description: Specifies and retrieves the object identifier (OID) of the hash algorithm used to sign the certificate request.
old-location: security\ix509certificaterequest_hashalgorithm_property.htm
old-project: SecCertEnroll
ms.assetid: 9f68ee54-5dea-47bb-8a90-0285d081c9b8
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security], IX509CertificateRequest interface, IX509CertificateRequest, IX509CertificateRequest interface [Security], HashAlgorithm property, IX509CertificateRequest.HashAlgorithm, IX509CertificateRequest::get_HashAlgorithm, IX509CertificateRequest::put_HashAlgorithm, certenroll/IX509CertificateRequest::HashAlgorithm, certenroll/IX509CertificateRequest::get_HashAlgorithm, certenroll/IX509CertificateRequest::put_HashAlgorithm, get_HashAlgorithm,IX509CertificateRequest.get_HashAlgorithm, security.ix509certificaterequest_hashalgorithm_property
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
-	IX509CertificateRequest.HashAlgorithm
-	IX509CertificateRequest.get_HashAlgorithm
-	IX509CertificateRequest.put_HashAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::get_HashAlgorithm method


## -description


The <b>HashAlgorithm</b> property specifies and retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the hash algorithm used to sign the certificate request. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If the certificate request contains nested requests and you set the <b>HashAlgorithm</b> property on the top level request, it is automatically propagated to all of the inner requests, overwriting values that may have been previously set. You can, however, set the property manually on each of the inner objects.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

