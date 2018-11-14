---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NullSigned
title: IX509CertificateRequestCmc::get_NullSigned
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether the primary signature on the certificate request is null-signed.
old-location: security\ix509certificaterequestcmc_nullsigned_property.htm
tech.root: SecCertEnroll
ms.assetid: 99cefeed-caec-401e-bdcd-d167472b2cbd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],NullSigned property, IX509CertificateRequestCmc.NullSigned, IX509CertificateRequestCmc.get_NullSigned, IX509CertificateRequestCmc::NullSigned, IX509CertificateRequestCmc::get_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NullSigned, certenroll/IX509CertificateRequestCmc::get_NullSigned, get_NullSigned, security.ix509certificaterequestcmc_nullsigned_property
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
 - IX509CertificateRequestCmc.NullSigned
 - IX509CertificateRequestCmc.get_NullSigned
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
- IX509CertificateRequestCmc.get_NullSigned
: 
---

# IX509CertificateRequestCmc::get_NullSigned


## -description


The <b>NullSigned</b> property retrieves a Boolean value that specifies whether the primary signature  on the certificate request is null-signed.

This property is read-only.


## -parameters


## -remarks



A null-signed certificate request is not really signed. That is, the request can be digested by using a digest algorithm such as SHA-1, but it is not encrypted with a public key algorithm such as RSA. This can be used when a private key is not available as is often the case when <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authorities</a> are being cross-certified.

You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
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
 

 

