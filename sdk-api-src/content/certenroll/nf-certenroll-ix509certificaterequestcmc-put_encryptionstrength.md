---
UID: NF:certenroll.IX509CertificateRequestCmc.put_EncryptionStrength
title: IX509CertificateRequestCmc::put_EncryptionStrength
author: windows-sdk-content
description: Specifies or retrieves the relative encryption level applied to the private key to be archived.
old-location: security\ix509certificaterequestcmc_encryptionstrength_property.htm
tech.root: seccertenroll
ms.assetid: 9cade9f0-d614-4838-bf42-0a19b4ce53d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EncryptionStrength property [Security], EncryptionStrength property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],EncryptionStrength property, IX509CertificateRequestCmc.EncryptionStrength, IX509CertificateRequestCmc.put_EncryptionStrength, IX509CertificateRequestCmc::EncryptionStrength, IX509CertificateRequestCmc::get_EncryptionStrength, IX509CertificateRequestCmc::put_EncryptionStrength, certenroll/IX509CertificateRequestCmc::EncryptionStrength, certenroll/IX509CertificateRequestCmc::get_EncryptionStrength, certenroll/IX509CertificateRequestCmc::put_EncryptionStrength, put_EncryptionStrength, security.ix509certificaterequestcmc_encryptionstrength_property
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
 - IX509CertificateRequestCmc.EncryptionStrength
 - IX509CertificateRequestCmc.get_EncryptionStrength
 - IX509CertificateRequestCmc.put_EncryptionStrength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::put_EncryptionStrength


## -description


The <b>EncryptionStrength</b> property specifies or retrieves the relative encryption level applied to the private key to be archived.

This property is read/write.


## -parameters


## -remarks



This property is related to the following properties:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377134(v=VS.85).aspx">ArchivePrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377243(v=VS.85).aspx">EncryptedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377244(v=VS.85).aspx">EncryptionAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377262(v=VS.85).aspx">KeyArchivalCertificate</a>
</li>
</ul>


The encryption strength is often implied by the encryption algorithm. If the algorithm does not support multiple strengths, you should not set the <b>EncryptionStrength</b> property.

You must set this property, if at all,  before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
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
 

 

