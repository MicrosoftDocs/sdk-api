---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SuppressOids
title: IX509CertificateRequestCmc::get_SuppressOids
author: windows-sdk-content
description: Retrieves a collection of extension or attribute object identifiers (OIDs) to be suppressed from the certificate during the encoding process.
old-location: security\ix509certificaterequestcmc_suppressoids_property.htm
tech.root: SecCertEnroll
ms.assetid: 6e0a8245-1bcc-413a-865a-8a6274dd55f5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SuppressOids property, IX509CertificateRequestCmc.SuppressOids, IX509CertificateRequestCmc.get_SuppressOids, IX509CertificateRequestCmc::SuppressOids, IX509CertificateRequestCmc::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SuppressOids, certenroll/IX509CertificateRequestCmc::get_SuppressOids, get_SuppressOids, security.ix509certificaterequestcmc_suppressoids_property
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
 - IX509CertificateRequestCmc.SuppressOids
 - IX509CertificateRequestCmc.get_SuppressOids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_SuppressOids


## -description


The <b>SuppressOids</b> property retrieves a collection of extension or attribute <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) to be suppressed from the certificate during the encoding process.

This property is read-only.


## -parameters


## -remarks



Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="https://msdn.microsoft.com/3a7847b6-52b4-4058-8113-cbc3b9101a5b">SuppressDefaults</a> property. For a CMC request, only the XCN_OID_REQUEST_CLIENT_INFO
(<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>) attribute is created by default. No extensions are added by default.

You must initialize the <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/be0e2cda-5481-49ab-9a12-6dc52981fd24">Initialize</a>
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
 

 

