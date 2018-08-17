---
UID: NF:certenroll.IX509CertificateRequestCmc.put_SenderNonce
title: IX509CertificateRequestCmc::put_SenderNonce
author: windows-sdk-content
description: Specifies or retrieves a byte array that contains a nonce.
old-location: security\ix509certificaterequestcmc_sendernonce_property.htm
old-project: seccertenroll
ms.assetid: 7f7ec18f-7b5b-445e-9033-12d86b3675f1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SenderNonce property, IX509CertificateRequestCmc.SenderNonce, IX509CertificateRequestCmc.put_SenderNonce, IX509CertificateRequestCmc::SenderNonce, IX509CertificateRequestCmc::get_SenderNonce, IX509CertificateRequestCmc::put_SenderNonce, SenderNonce property [Security], SenderNonce property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SenderNonce, certenroll/IX509CertificateRequestCmc::get_SenderNonce, certenroll/IX509CertificateRequestCmc::put_SenderNonce, put_SenderNonce, security.ix509certificaterequestcmc_sendernonce_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - IX509CertificateRequestCmc.SenderNonce
 - IX509CertificateRequestCmc.get_SenderNonce
 - IX509CertificateRequestCmc.put_SenderNonce
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::put_SenderNonce


## -description


The <b>SenderNonce</b> property specifies or retrieves a byte array that contains a nonce. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read/write.


## -parameters


## -remarks



A nonce is single use, random or pseudo-random byte array that can be included in a certificate request to help ensure that the request is not a repeat of a previous message.

You can set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377610(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377613(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377616(v=VS.85).aspx">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377257(v=VS.85).aspx">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377622(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>
 

 

