---
UID: NF:certenroll.IX509CertificateRequest.put_Silent
title: IX509CertificateRequest::put_Silent
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether any of the key-related modal dialogs are displayed during the certificate enrollment process.
old-location: security\ix509certificaterequest_silent_property.htm
tech.root: seccertenroll
ms.assetid: 339c8d47-4406-4f2e-b927-b2dd5f58d1ec
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequest interface [Security],Silent property, IX509CertificateRequest.Silent, IX509CertificateRequest.put_Silent, IX509CertificateRequest::Silent, IX509CertificateRequest::get_Silent, IX509CertificateRequest::put_Silent, Silent property [Security], Silent property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::Silent, certenroll/IX509CertificateRequest::get_Silent, certenroll/IX509CertificateRequest::put_Silent, put_Silent, security.ix509certificaterequest_silent_property
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
 - IX509CertificateRequest.Silent
 - IX509CertificateRequest.get_Silent
 - IX509CertificateRequest.put_Silent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::put_Silent


## -description


The <b>Silent</b> property specifies or retrieves a Boolean value that indicates whether any of the  key-related modal dialogs are displayed during the certificate enrollment process.

This property is read/write.


## -parameters


## -remarks



This property value is used by key-related Certificate Enrollment Control modal dialogs that:<ul>
<li>Direct a user to insert a smart card</li>
<li>Request a smart card pin number</li>
<li>Request the  protection level for a new key</li>
<li>Request a user password before accessing a key</li>
</ul>


You can set this property before calling any initialization  method or the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method. For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the property value is updated on the inner request and all signing certificates.

If the certificate request contains nested requests and you set the <b>Silent</b> property on the top level request, it is automatically propagated to all of the inner requests. You can, however, set the property manually on each of the inner objects.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

