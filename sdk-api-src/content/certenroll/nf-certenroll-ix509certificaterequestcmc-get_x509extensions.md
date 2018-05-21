---
UID: NF:certenroll.IX509CertificateRequestCmc.get_X509Extensions
title: IX509CertificateRequestCmc::get_X509Extensions
author: windows-driver-content
description: Retrieves a collection of the extensions included in the certificate request.
old-location: security\ix509certificaterequestcmc_x509extensions_property.htm
old-project: SecCertEnroll
ms.assetid: 75eae625-5c41-4eef-aacd-bd1681286b2b
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],X509Extensions property, IX509CertificateRequestCmc.X509Extensions, IX509CertificateRequestCmc.get_X509Extensions, IX509CertificateRequestCmc::X509Extensions, IX509CertificateRequestCmc::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::X509Extensions, certenroll/IX509CertificateRequestCmc::get_X509Extensions, get_X509Extensions, security.ix509certificaterequestcmc_x509extensions_property
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
-	IX509CertificateRequestCmc.X509Extensions
-	IX509CertificateRequestCmc.get_X509Extensions
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_X509Extensions


## -description


The <b>X509Extensions</b> property retrieves a collection of the extensions included in the certificate request.

This property is read-only.


## -parameters


## -remarks



You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/40084cb0-eb48-485d-aa45-8ddb577f2d4f">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7500b714-4608-4da6-85ad-20cea30853cc">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b63bfaaa-a8af-4c72-a191-447230adae72">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/abf7617e-1194-4303-a214-23fbaf20eccf">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d6c15fcb-1883-4d87-af29-721102676535">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>
 

 

