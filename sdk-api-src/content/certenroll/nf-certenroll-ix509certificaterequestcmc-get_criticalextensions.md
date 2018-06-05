---
UID: NF:certenroll.IX509CertificateRequestCmc.get_CriticalExtensions
title: IX509CertificateRequestCmc::get_CriticalExtensions
author: windows-sdk-content
description: Retrieves an IObjectIds collection that identifies the version 3 certificate extensions marked as critical.
old-location: security\ix509certificaterequestcmc_criticalextensions_property.htm
old-project: SecCertEnroll
ms.assetid: 06c5d148-eecc-45db-9d82-ec56c226ffed
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CriticalExtensions property [Security], CriticalExtensions property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],CriticalExtensions property, IX509CertificateRequestCmc.CriticalExtensions, IX509CertificateRequestCmc.get_CriticalExtensions, IX509CertificateRequestCmc::CriticalExtensions, IX509CertificateRequestCmc::get_CriticalExtensions, certenroll/IX509CertificateRequestCmc::CriticalExtensions, certenroll/IX509CertificateRequestCmc::get_CriticalExtensions, get_CriticalExtensions, security.ix509certificaterequestcmc_criticalextensions_property
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
-	IX509CertificateRequestCmc.CriticalExtensions
-	IX509CertificateRequestCmc.get_CriticalExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_CriticalExtensions


## -description


The <b>CriticalExtensions</b> property retrieves an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

This property is read-only.


## -parameters


## -remarks



The extension criticality indicates to an application that uses certificates whether it can ignore the extension. You must initialize the CMC request object before calling this property. For more information, see the following topics:

<ul>
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
 

 

