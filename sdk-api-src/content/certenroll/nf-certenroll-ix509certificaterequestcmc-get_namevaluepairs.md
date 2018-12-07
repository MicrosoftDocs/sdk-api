---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NameValuePairs
title: IX509CertificateRequestCmc::get_NameValuePairs
author: windows-sdk-content
description: Retrieves an IX509NameValuePairs collection associated with a certificate request.
old-location: security\ix509certificaterequestcmc_namevaluepairs_property.htm
tech.root: seccertenroll
ms.assetid: 3b98629e-a501-4ba0-8825-0cab7187d6f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],NameValuePairs property, IX509CertificateRequestCmc.NameValuePairs, IX509CertificateRequestCmc.get_NameValuePairs, IX509CertificateRequestCmc::NameValuePairs, IX509CertificateRequestCmc::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NameValuePairs, certenroll/IX509CertificateRequestCmc::get_NameValuePairs, get_NameValuePairs, security.ix509certificaterequestcmc_namevaluepairs_property
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
 - IX509CertificateRequestCmc.NameValuePairs
 - IX509CertificateRequestCmc.get_NameValuePairs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_NameValuePairs


## -description


The <b>NameValuePairs</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa378746(v=VS.85).aspx">IX509NameValuePairs</a> collection associated with a certificate request.

This property is read-only.


## -parameters


## -remarks



For an example of a name-value pair in a CMC request object, see <a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">IX509NameValuePair</a>. You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
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
 

 

