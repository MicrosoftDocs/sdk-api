---
UID: NF:certenroll.IX509CertificateRequestCmc.get_CryptAttributes
title: IX509CertificateRequestCmc::get_CryptAttributes
author: windows-sdk-content
description: Retrieves an ICryptAttributes collection of optional certificate attributes.
old-location: security\ix509certificaterequestcmc_cryptattributes_property.htm
old-project: SecCertEnroll
ms.assetid: 733d29d8-95ea-4193-99b0-a07fcf560435
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CryptAttributes property [Security], CryptAttributes property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],CryptAttributes property, IX509CertificateRequestCmc.CryptAttributes, IX509CertificateRequestCmc.get_CryptAttributes, IX509CertificateRequestCmc::CryptAttributes, IX509CertificateRequestCmc::get_CryptAttributes, certenroll/IX509CertificateRequestCmc::CryptAttributes, certenroll/IX509CertificateRequestCmc::get_CryptAttributes, get_CryptAttributes, security.ix509certificaterequestcmc_cryptattributes_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestCmc.CryptAttributes
-	IX509CertificateRequestCmc.get_CryptAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_CryptAttributes


## -description


The <b>CryptAttributes</b> property retrieves an <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection of optional certificate attributes.

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
 

 

