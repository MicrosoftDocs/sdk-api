---
UID: NF:certenroll.IX509CertificateRequest.get_ParentWindow
title: IX509CertificateRequest::get_ParentWindow
author: windows-sdk-content
description: Specifies and retrieves the ID of the window used by key-related user interface dialogs.
old-location: security\ix509certificaterequest_parentwindow_property.htm
old-project: seccertenroll
ms.assetid: 86e82a6c-7689-4bf3-8f64-e512040abd6a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequest interface [Security],ParentWindow property, IX509CertificateRequest.ParentWindow, IX509CertificateRequest.get_ParentWindow, IX509CertificateRequest::ParentWindow, IX509CertificateRequest::get_ParentWindow, IX509CertificateRequest::put_ParentWindow, ParentWindow property [Security], ParentWindow property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::ParentWindow, certenroll/IX509CertificateRequest::get_ParentWindow, certenroll/IX509CertificateRequest::put_ParentWindow, get_ParentWindow, security.ix509certificaterequest_parentwindow_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.ParentWindow
 - IX509CertificateRequest.get_ParentWindow
 - IX509CertificateRequest.put_ParentWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::get_ParentWindow


## -description


The <b>ParentWindow</b> property specifies and retrieves the ID of the window used by key-related user interface dialogs.

This property is read/write.


## -parameters


## -remarks



This property value is used by key-related Certificate Enrollment Control modal dialogs that:<ul>
<li>Direct a user to insert a smart card</li>
<li>Request a smart card pin number</li>
<li>Request the  protection level for a new key</li>
<li>Request a user password before accessing a key</li>
</ul>


If your application uses key-related modal dialogs, we recommend that you use this property to ensure that your window displays in front of other windows and that the requested action is performed before the thread can be unblocked.

You can set this property before calling any initialization method or the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method. If the certificate request contains nested requests and you set the <b>ParentWindow</b> property on the top level request, it is automatically propagated to all of the inner requests. You can, however, set the property manually on each of the inner objects.

For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the window ID is updated on the inner request and all signing certificates.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

