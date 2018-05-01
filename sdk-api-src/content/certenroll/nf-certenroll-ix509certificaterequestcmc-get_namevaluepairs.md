---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NameValuePairs
title: IX509CertificateRequestCmc::get_NameValuePairs method
author: windows-driver-content
description: Retrieves an IX509NameValuePairs collection associated with a certificate request.
old-location: security\ix509certificaterequestcmc_namevaluepairs_property.htm
old-project: SecCertEnroll
ms.assetid: 3b98629e-a501-4ba0-8825-0cab7187d6f5
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509CertificateRequestCmc, IX509CertificateRequestCmc interface [Security], NameValuePairs property, IX509CertificateRequestCmc.NameValuePairs, IX509CertificateRequestCmc::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security], IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NameValuePairs, certenroll/IX509CertificateRequestCmc::get_NameValuePairs, get_NameValuePairs,IX509CertificateRequestCmc.get_NameValuePairs, security.ix509certificaterequestcmc_namevaluepairs_property
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
-	IX509CertificateRequestCmc.NameValuePairs
-	IX509CertificateRequestCmc.get_NameValuePairs
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_NameValuePairs method


## -description


The <b>NameValuePairs</b> property retrieves an <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> collection associated with a certificate request.

This property is read-only.


## -parameters


## -remarks



For an example of a name-value pair in a CMC request object, see <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a>. You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
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
 

 

