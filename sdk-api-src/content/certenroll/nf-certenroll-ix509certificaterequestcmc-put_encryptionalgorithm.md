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


The <b>EncryptionAlgorithm</b> property specifies or retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the algorithm used to encrypt the private key to be archived. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



When you request that a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) archive your private key, you must retrieve an exchange certificate from the CA and use the public key contained in that certificate to encrypt the private key that you are submitting for archival. The <b>EncryptionAlgorithm</b> property identifies the algorithm used to encrypt your key.

This property is related to the following properties:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377134(v=VS.85).aspx">ArchivePrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377243(v=VS.85).aspx">EncryptedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377250(v=VS.85).aspx">EncryptionStrength</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377262(v=VS.85).aspx">KeyArchivalCertificate</a>
</li>
</ul>


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
 

 

