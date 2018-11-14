---
UID: NF:certenroll.IX509CertificateRequestCmc.put_KeyArchivalCertificate
title: IX509CertificateRequestCmc::put_KeyArchivalCertificate
author: windows-sdk-content
description: Specifies or retrieves a certification authority (CA) encryption certificate.
old-location: security\ix509certificaterequestcmc_keyarchivalcertificate_property.htm
tech.root: SecCertEnroll
ms.assetid: 93f71fd7-33bb-4352-b184-7270bca1363f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],KeyArchivalCertificate property, IX509CertificateRequestCmc.KeyArchivalCertificate, IX509CertificateRequestCmc.put_KeyArchivalCertificate, IX509CertificateRequestCmc::KeyArchivalCertificate, IX509CertificateRequestCmc::get_KeyArchivalCertificate, IX509CertificateRequestCmc::put_KeyArchivalCertificate, KeyArchivalCertificate property [Security], KeyArchivalCertificate property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::get_KeyArchivalCertificate, certenroll/IX509CertificateRequestCmc::put_KeyArchivalCertificate, put_KeyArchivalCertificate, security.ix509certificaterequestcmc_keyarchivalcertificate_property
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
 - IX509CertificateRequestCmc.KeyArchivalCertificate
 - IX509CertificateRequestCmc.get_KeyArchivalCertificate
 - IX509CertificateRequestCmc.put_KeyArchivalCertificate
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
- IX509CertificateRequestCmc.put_KeyArchivalCertificate
: 
---

# IX509CertificateRequestCmc::put_KeyArchivalCertificate


## -description


The <b>KeyArchivalCertificate</b> property specifies or retrieves a certification authority (CA) encryption certificate. The certificate is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If correctly configured, a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) can archive a client's private key. Typically, the client requests an exchange certificate from the CA, validates it, and uses it as input to the <b>KeyArchivalCertificate</b> property. The CA's public key is used to encrypt the private key that is being submitted for archiving. You can use the <a href="https://msdn.microsoft.com/en-us/library/Aa377134(v=VS.85).aspx">ArchivePrivateKey</a> property to request key archival.

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
 

 

