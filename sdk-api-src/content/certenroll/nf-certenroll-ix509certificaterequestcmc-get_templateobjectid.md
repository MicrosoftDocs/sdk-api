---
UID: NF:certenroll.IX509CertificateRequestCmc.get_TemplateObjectId
title: IX509CertificateRequestCmc::get_TemplateObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID) of the template used to create the certificate request.
old-location: security\ix509certificaterequestcmc_templateobjectid_property.htm
old-project: seccertenroll
ms.assetid: 36a87e0e-d910-45a7-9850-512ff94e78b8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],TemplateObjectId property, IX509CertificateRequestCmc.TemplateObjectId, IX509CertificateRequestCmc.get_TemplateObjectId, IX509CertificateRequestCmc::TemplateObjectId, IX509CertificateRequestCmc::get_TemplateObjectId, TemplateObjectId property [Security], TemplateObjectId property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::TemplateObjectId, certenroll/IX509CertificateRequestCmc::get_TemplateObjectId, get_TemplateObjectId, security.ix509certificaterequestcmc_templateobjectid_property
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestCmc.TemplateObjectId
 - IX509CertificateRequestCmc.get_TemplateObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_TemplateObjectId


## -description


The <b>TemplateObjectId</b> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the template used to create the certificate request.

This property is read-only.


## -parameters


## -remarks



The object identifier can be an OID for the Active Directory Common Name (CN) of the template. You must initialize the <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

