---
UID: NF:certenroll.IX509CertificateRequestCmc.get_CryptAttributes
title: IX509CertificateRequestCmc::get_CryptAttributes
author: windows-sdk-content
description: Retrieves an ICryptAttributes collection of optional certificate attributes.
old-location: security\ix509certificaterequestcmc_cryptattributes_property.htm
tech.root: seccertenroll
ms.assetid: 733d29d8-95ea-4193-99b0-a07fcf560435
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptAttributes property [Security], CryptAttributes property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],CryptAttributes property, IX509CertificateRequestCmc.CryptAttributes, IX509CertificateRequestCmc.get_CryptAttributes, IX509CertificateRequestCmc::CryptAttributes, IX509CertificateRequestCmc::get_CryptAttributes, certenroll/IX509CertificateRequestCmc::CryptAttributes, certenroll/IX509CertificateRequestCmc::get_CryptAttributes, get_CryptAttributes, security.ix509certificaterequestcmc_cryptattributes_property
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
 - IX509CertificateRequestCmc.CryptAttributes
 - IX509CertificateRequestCmc.get_CryptAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_CryptAttributes


## -description


The <b>CryptAttributes</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection of optional certificate attributes.

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
 

 

