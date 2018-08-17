---
UID: NF:certenroll.IX509CertificateRequestCmc.put_ArchivePrivateKey
title: IX509CertificateRequestCmc::put_ArchivePrivateKey
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).
old-location: security\ix509certificaterequestcmc_archiveprivatekey_property.htm
old-project: seccertenroll
ms.assetid: 6d17222e-3657-4911-a8e7-d90214284441
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ArchivePrivateKey property [Security], ArchivePrivateKey property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],ArchivePrivateKey property, IX509CertificateRequestCmc.ArchivePrivateKey, IX509CertificateRequestCmc.put_ArchivePrivateKey, IX509CertificateRequestCmc::ArchivePrivateKey, IX509CertificateRequestCmc::get_ArchivePrivateKey, IX509CertificateRequestCmc::put_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::get_ArchivePrivateKey, certenroll/IX509CertificateRequestCmc::put_ArchivePrivateKey, put_ArchivePrivateKey, security.ix509certificaterequestcmc_archiveprivatekey_property
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
 - IX509CertificateRequestCmc.ArchivePrivateKey
 - IX509CertificateRequestCmc.get_ArchivePrivateKey
 - IX509CertificateRequestCmc.put_ArchivePrivateKey
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCmc::put_ArchivePrivateKey


## -description


The <b>ArchivePrivateKey</b> property specifies or retrieves a Boolean value that indicates whether to archive a private key on the certification authority (CA).

This property is read/write.


## -parameters


## -remarks



To request that a CA archive your private key, you must also set the <a href="https://msdn.microsoft.com/en-us/library/Aa377262(v=VS.85).aspx">KeyArchivalCertificate</a> property with the CA encryption (key exchange) certificate.

You can set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, but you must initialize the CMC request object before setting the property value. For more information, see the following topics:<ul>
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
 

 

