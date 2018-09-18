---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SenderNonce
title: IX509CertificateRequestCmc::get_SenderNonce
author: windows-sdk-content
description: Specifies or retrieves a byte array that contains a nonce.
old-location: security\ix509certificaterequestcmc_sendernonce_property.htm
tech.root: seccertenroll
ms.assetid: 7f7ec18f-7b5b-445e-9033-12d86b3675f1
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SenderNonce property, IX509CertificateRequestCmc.SenderNonce, IX509CertificateRequestCmc.get_SenderNonce, IX509CertificateRequestCmc::SenderNonce, IX509CertificateRequestCmc::get_SenderNonce, IX509CertificateRequestCmc::put_SenderNonce, SenderNonce property [Security], SenderNonce property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SenderNonce, certenroll/IX509CertificateRequestCmc::get_SenderNonce, certenroll/IX509CertificateRequestCmc::put_SenderNonce, get_SenderNonce, security.ix509certificaterequestcmc_sendernonce_property
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
 - IX509CertificateRequestCmc.SenderNonce
 - IX509CertificateRequestCmc.get_SenderNonce
 - IX509CertificateRequestCmc.put_SenderNonce
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_SenderNonce


## -description


The <b>SenderNonce</b> property specifies or retrieves a byte array that contains a nonce. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read/write.


## -parameters


## -remarks



A nonce is single use, random or pseudo-random byte array that can be included in a certificate request to help ensure that the request is not a repeat of a previous message.

You can set this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
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
 

 

