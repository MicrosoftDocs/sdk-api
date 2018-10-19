---
UID: NF:certenroll.IX509CertificateRequestCmc.put_ArchivePrivateKey
title: IX509CertificateRequestCmc::put_ArchivePrivateKey
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).
old-location: security\ix509certificaterequestcmc_archiveprivatekey_property.htm
tech.root: SecCertEnroll
ms.assetid: 6d17222e-3657-4911-a8e7-d90214284441
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ArchivePrivateKey property [Security], ArchivePrivateKey property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],ArchivePrivateKey property, IX509CertificateRequestCmc.ArchivePrivateKey, IX509CertificateRequestCmc.put_ArchivePrivateKey, IX509CertificateRequestCmc::ArchivePrivateKey, IX509CertificateRequestCmc::get_ArchivePrivateKey, IX509CertificateRequestCmc::put_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::get_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::put_ArchivePrivateKey, put_ArchivePrivateKey, security.ix509certificaterequestcmc_archiveprivatekey_property
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
 - IX509CertificateRequestCmc.ArchivePrivateKey
 - IX509CertificateRequestCmc.get_ArchivePrivateKey
 - IX509CertificateRequestCmc.put_ArchivePrivateKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::put_ArchivePrivateKey


## -description


The <b>ArchivePrivateKey</b> property specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).

This property is read/write.


## -parameters


## -remarks



To request that a CA archive your private key, you must also set the <a href="https://msdn.microsoft.com/93f71fd7-33bb-4352-b184-7270bca1363f">KeyArchivalCertificate</a> property with the CA encryption (key exchange) certificate.

You can set this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, but you must initialize the CMC request object before setting the property value. For more information, see the following topics:<ul>
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
 

 

