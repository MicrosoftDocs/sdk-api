---
UID: NF:certenroll.IX509CertificateRequestCmc.put_EncryptionStrength
title: IX509CertificateRequestCmc::put_EncryptionStrength (certenroll.h)
author: windows-sdk-content
description: Specifies or retrieves the relative encryption level applied to the private key to be archived.
old-location: security\ix509certificaterequestcmc_encryptionstrength_property.htm
tech.root: seccertenroll
ms.assetid: 9cade9f0-d614-4838-bf42-0a19b4ce53d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EncryptionStrength property [Security], EncryptionStrength property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptionStrength property, IX509CertificateRequestCmc.EncryptionStrength, IX509CertificateRequestCmc.put_EncryptionStrength, IX509CertificateRequestCmc::EncryptionStrength, IX509CertificateRequestCmc::get_EncryptionStrength, IX509CertificateRequestCmc::put_EncryptionStrength, certenroll/IX509CertificateRequestCmc::EncryptionStrength, certenroll/IX509CertificateRequestCmc::get_EncryptionStrength, certenroll/IX509CertificateRequestCmc::put_EncryptionStrength, put_EncryptionStrength, security.ix509certificaterequestcmc_encryptionstrength_property
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
 - IX509CertificateRequestCmc.EncryptionStrength
 - IX509CertificateRequestCmc.get_EncryptionStrength
 - IX509CertificateRequestCmc.put_EncryptionStrength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestCmc::put_EncryptionStrength


## -description


The <b>EncryptionStrength</b> property specifies or retrieves the relative encryption level applied to the private key to be archived.

This property is read/write.


## -parameters


## -remarks



This property is related to the following properties:<ul>
<li>
<a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63aba8aa-bee7-46b6-a821-4e4d440356ac">EncryptedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c46b3373-6d9e-46d9-a36a-b73a718ddaf7">EncryptionAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93f71fd7-33bb-4352-b184-7270bca1363f">KeyArchivalCertificate</a>
</li>
</ul>


The encryption strength is often implied by the encryption algorithm. If the algorithm does not support multiple strengths, you should not set the <b>EncryptionStrength</b> property.

You must set this property, if at all,  before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
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
 

 

