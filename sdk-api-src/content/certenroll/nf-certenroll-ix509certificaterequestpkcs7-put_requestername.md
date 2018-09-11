---
UID: NF:certenroll.IX509CertificateRequestPkcs7.put_RequesterName
title: IX509CertificateRequestPkcs7::put_RequesterName
author: windows-sdk-content
description: Specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate.
old-location: security\ix509certificaterequestpkcs7_requestername_property.htm
tech.root: SecCertEnroll
ms.assetid: af85e976-cc79-4285-b553-a8001e84ec68
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],RequesterName property, IX509CertificateRequestPkcs7.RequesterName, IX509CertificateRequestPkcs7.put_RequesterName, IX509CertificateRequestPkcs7::RequesterName, IX509CertificateRequestPkcs7::get_RequesterName, IX509CertificateRequestPkcs7::put_RequesterName, RequesterName property [Security], RequesterName property [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::RequesterName, certenroll/IX509CertificateRequestPkcs7::get_RequesterName, certenroll/IX509CertificateRequestPkcs7::put_RequesterName, put_RequesterName, security.ix509certificaterequestpkcs7_requestername_property
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
 - IX509CertificateRequestPkcs7.RequesterName
 - IX509CertificateRequestPkcs7.get_RequesterName
 - IX509CertificateRequestPkcs7.put_RequesterName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs7::put_RequesterName


## -description


The <b>RequesterName</b> property specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



This property is only used when the enrollment agent is enrolling on behalf of another user. You must initialize the PKCS #7 request object before calling this property. For more information, see the following topics:<ul>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377622(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
 

 

