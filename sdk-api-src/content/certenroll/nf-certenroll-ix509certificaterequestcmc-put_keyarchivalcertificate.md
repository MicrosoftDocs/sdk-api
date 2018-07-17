---
UID: NF:certenroll.IX509CertificateRequestCmc.put_KeyArchivalCertificate
title: IX509CertificateRequestCmc::put_KeyArchivalCertificate
author: windows-sdk-content
description: Specifies or retrieves a certification authority (CA) encryption certificate.
old-location: security\ix509certificaterequestcmc_keyarchivalcertificate_property.htm
old-project: seccertenroll
ms.assetid: 93f71fd7-33bb-4352-b184-7270bca1363f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],KeyArchivalCertificate property, IX509CertificateRequestCmc.KeyArchivalCertificate, IX509CertificateRequestCmc.put_KeyArchivalCertificate, IX509CertificateRequestCmc::KeyArchivalCertificate, IX509CertificateRequestCmc::get_KeyArchivalCertificate, IX509CertificateRequestCmc::put_KeyArchivalCertificate, KeyArchivalCertificate property [Security], KeyArchivalCertificate property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::get_KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::put_KeyArchivalCertificate, put_KeyArchivalCertificate, security.ix509certificaterequestcmc_keyarchivalcertificate_property
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
 - IX509CertificateRequestCmc.KeyArchivalCertificate
 - IX509CertificateRequestCmc.get_KeyArchivalCertificate
 - IX509CertificateRequestCmc.put_KeyArchivalCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::put_KeyArchivalCertificate


## -description


The <b>KeyArchivalCertificate</b> property specifies or retrieves a certification authority (CA) encryption certificate. The certificate is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If correctly configured, a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) can archive a client's private key. Typically, the client requests an exchange certificate from the CA, validates it, and uses it as input to the <b>KeyArchivalCertificate</b> property. The CA's public key is used to encrypt the private key that is being submitted for archiving. You can use the <a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a> property to request key archival.

You must set this property, if at all,  before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
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
 

 

