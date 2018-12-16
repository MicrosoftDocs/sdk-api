---
UID: NF:certenroll.IX509CertificateRequest.put_UIContextMessage
title: IX509CertificateRequest::put_UIContextMessage
author: windows-sdk-content
description: Specifies or retrieves a context string to display in the user interface.
old-location: security\ix509certificaterequest_uicontextmessage_property.htm
tech.root: seccertenroll
ms.assetid: 0eedb520-06c3-4106-8593-1c5fb0829d5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequest interface [Security],UIContextMessage property, IX509CertificateRequest.UIContextMessage, IX509CertificateRequest.put_UIContextMessage, IX509CertificateRequest::UIContextMessage, IX509CertificateRequest::get_UIContextMessage, IX509CertificateRequest::put_UIContextMessage, UIContextMessage property [Security], UIContextMessage property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::UIContextMessage, certenroll/IX509CertificateRequest::get_UIContextMessage, certenroll/IX509CertificateRequest::put_UIContextMessage, put_UIContextMessage, security.ix509certificaterequest_uicontextmessage_property
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
 - IX509CertificateRequest.UIContextMessage
 - IX509CertificateRequest.get_UIContextMessage
 - IX509CertificateRequest.put_UIContextMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::put_UIContextMessage


## -description


The <b>UIContextMessage</b> property specifies or retrieves a context string to display in the user interface.

This property is read/write.


## -parameters


## -remarks



You can set this property before calling any initialization method or the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method. For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the property value is updated on the inner request and all signing certificates.

The context string should include additional information about an action. For example, if the user interface instructs the user to enter a smartcard PIN, the context string can indicate that a PIN is used to verify the identity of the user so that the request can be signed.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

