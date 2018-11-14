---
UID: NF:certenroll.IX509CertificateRequestCmc.get_X509Extensions
title: IX509CertificateRequestCmc::get_X509Extensions
author: windows-sdk-content
description: Retrieves a collection of the extensions included in the certificate request.
old-location: security\ix509certificaterequestcmc_x509extensions_property.htm
tech.root: SecCertEnroll
ms.assetid: 75eae625-5c41-4eef-aacd-bd1681286b2b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],X509Extensions property, IX509CertificateRequestCmc.X509Extensions, IX509CertificateRequestCmc.get_X509Extensions, IX509CertificateRequestCmc::X509Extensions, IX509CertificateRequestCmc::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::X509Extensions, certenroll/IX509CertificateRequestCmc::get_X509Extensions, get_X509Extensions, security.ix509certificaterequestcmc_x509extensions_property
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
 - IX509CertificateRequestCmc.X509Extensions
 - IX509CertificateRequestCmc.get_X509Extensions
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
- IX509CertificateRequestCmc.get_X509Extensions
: 
---

# IX509CertificateRequestCmc::get_X509Extensions


## -description


The <b>X509Extensions</b> property retrieves a collection of the extensions included in the certificate request.

This property is read-only.


## -parameters


## -remarks



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
 

 

