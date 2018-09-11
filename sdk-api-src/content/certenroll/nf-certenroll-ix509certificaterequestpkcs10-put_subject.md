---
UID: NF:certenroll.IX509CertificateRequestPkcs10.put_Subject
title: IX509CertificateRequestPkcs10::put_Subject
author: windows-sdk-content
description: Specifies or retrieves the X.500 distinguished name of the entity requesting the certificate.
old-location: security\ix509certificaterequestpkcs10_subject_property.htm
tech.root: SecCertEnroll
ms.assetid: 7b521586-f2fc-4b2f-83ab-79f9b972f9a1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],Subject property, IX509CertificateRequestPkcs10.Subject, IX509CertificateRequestPkcs10.put_Subject, IX509CertificateRequestPkcs10::Subject, IX509CertificateRequestPkcs10::get_Subject, IX509CertificateRequestPkcs10::put_Subject, Subject property [Security], Subject property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::Subject, certenroll/IX509CertificateRequestPkcs10::get_Subject, certenroll/IX509CertificateRequestPkcs10::put_Subject, put_Subject, security.ix509certificaterequestpkcs10_subject_property
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
 - IX509CertificateRequestPkcs10.Subject
 - IX509CertificateRequestPkcs10.get_Subject
 - IX509CertificateRequestPkcs10.put_Subject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::put_Subject


## -description


The <b>Subject</b> property specifies or retrieves the X.500 distinguished name of the entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



You must set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, and you must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

