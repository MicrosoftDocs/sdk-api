---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SuppressOids
title: IX509CertificateRequestCmc::get_SuppressOids
author: windows-sdk-content
description: Retrieves a collection of extension or attribute object identifiers (OIDs) to be suppressed from the certificate during the encoding process.
old-location: security\ix509certificaterequestcmc_suppressoids_property.htm
tech.root: SecCertEnroll
ms.assetid: 6e0a8245-1bcc-413a-865a-8a6274dd55f5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SuppressOids property, IX509CertificateRequestCmc.SuppressOids, IX509CertificateRequestCmc.get_SuppressOids, IX509CertificateRequestCmc::SuppressOids, IX509CertificateRequestCmc::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SuppressOids, certenroll/IX509CertificateRequestCmc::get_SuppressOids, get_SuppressOids, security.ix509certificaterequestcmc_suppressoids_property
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
 - IX509CertificateRequestCmc.SuppressOids
 - IX509CertificateRequestCmc.get_SuppressOids
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
- IX509CertificateRequestCmc.get_SuppressOids
: 
---

# IX509CertificateRequestCmc::get_SuppressOids


## -description


The <b>SuppressOids</b> property retrieves a collection of extension or attribute <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs) to be suppressed from the certificate during the encoding process.

This property is read-only.


## -parameters


## -remarks



Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377698(v=VS.85).aspx">SuppressDefaults</a> property. For a CMC request, only the XCN_OID_REQUEST_CLIENT_INFO
(<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>) attribute is created by default. No extensions are added by default.

You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

