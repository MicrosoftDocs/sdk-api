---
UID: NF:certenroll.IX509CertificateRequestCmc.put_EncryptionAlgorithm
title: IX509CertificateRequestCmc::put_EncryptionAlgorithm
author: windows-sdk-content
description: Specifies or retrieves an object identifier (OID) of the algorithm used to encrypt the private key to be archived.
old-location: security\ix509certificaterequestcmc_encryptionalgorithm_property.htm
tech.root: SecCertEnroll
ms.assetid: c46b3373-6d9e-46d9-a36a-b73a718ddaf7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EncryptionAlgorithm property [Security], EncryptionAlgorithm property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptionAlgorithm property, IX509CertificateRequestCmc.EncryptionAlgorithm, IX509CertificateRequestCmc.put_EncryptionAlgorithm, IX509CertificateRequestCmc::EncryptionAlgorithm, IX509CertificateRequestCmc::get_EncryptionAlgorithm, IX509CertificateRequestCmc::put_EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::get_EncryptionAlgorithm, certenroll/IX509CertificateRequestCmc::put_EncryptionAlgorithm, put_EncryptionAlgorithm, security.ix509certificaterequestcmc_encryptionalgorithm_property
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
 - IX509CertificateRequestCmc.EncryptionAlgorithm
 - IX509CertificateRequestCmc.get_EncryptionAlgorithm
 - IX509CertificateRequestCmc.put_EncryptionAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequestCmc.put_EncryptionAlgorithm
: 
---

# IX509CertificateRequestCmc::put_EncryptionAlgorithm


## -description


The <b>EncryptionAlgorithm</b> property specifies or retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the algorithm used to encrypt the private key to be archived. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



When you request that a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) archive your private key, you must retrieve an exchange certificate from the CA and use the public key contained in that certificate to encrypt the private key that you are submitting for archival. The <b>EncryptionAlgorithm</b> property identifies the algorithm used to encrypt your key.

This property is related to the following properties:<ul>
<li>
<a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63aba8aa-bee7-46b6-a821-4e4d440356ac">EncryptedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9cade9f0-d614-4838-bf42-0a19b4ce53d5">EncryptionStrength</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93f71fd7-33bb-4352-b184-7270bca1363f">KeyArchivalCertificate</a>
</li>
</ul>


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
 

 

