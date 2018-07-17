---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NullSigned
title: IX509CertificateRequestCmc::get_NullSigned
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether the primary signature on the certificate request is null-signed.
old-location: security\ix509certificaterequestcmc_nullsigned_property.htm
old-project: seccertenroll
ms.assetid: 99cefeed-caec-401e-bdcd-d167472b2cbd
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],NullSigned property, IX509CertificateRequestCmc.NullSigned, IX509CertificateRequestCmc.get_NullSigned, IX509CertificateRequestCmc::NullSigned, IX509CertificateRequestCmc::get_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NullSigned, certenroll/IX509CertificateRequestCmc::get_NullSigned, get_NullSigned, security.ix509certificaterequestcmc_nullsigned_property
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
 - IX509CertificateRequestCmc.NullSigned
 - IX509CertificateRequestCmc.get_NullSigned
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::get_NullSigned


## -description


The <b>NullSigned</b> property retrieves a Boolean value that specifies whether the primary signature  on the certificate request is null-signed.

This property is read-only.


## -parameters


## -remarks



A null-signed certificate request is not really signed. That is, the request can be digested by using a digest algorithm such as SHA-1, but it is not encrypted with a public key algorithm such as RSA. This can be used when a private key is not available as is often the case when <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> are being cross-certified.

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
 

 

