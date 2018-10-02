---
UID: NF:certenroll.IX509CertificateRequest.put_UIContextMessage
title: IX509CertificateRequest::put_UIContextMessage
author: windows-sdk-content
description: Specifies or retrieves a context string to display in the user interface.
old-location: security\ix509certificaterequest_uicontextmessage_property.htm
tech.root: SecCertEnroll
ms.assetid: 0eedb520-06c3-4106-8593-1c5fb0829d5e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequest interface [Security],UIContextMessage property, IX509CertificateRequest.UIContextMessage, IX509CertificateRequest.put_UIContextMessage, IX509CertificateRequest::UIContextMessage, IX509CertificateRequest::get_UIContextMessage, IX509CertificateRequest::put_UIContextMessage, UIContextMessage property [Security], UIContextMessage property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::UIContextMessage, certenroll/IX509CertificateRequest::get_UIContextMessage, certenroll/IX509CertificateRequest::put_UIContextMessage, put_UIContextMessage, security.ix509certificaterequest_uicontextmessage_property
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



You can set this property before calling any initialization method or the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method. For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the property value is updated on the inner request and all signing certificates.

The context string should include additional information about an action. For example, if the user interface instructs the user to enter a smartcard PIN, the context string can indicate that a PIN is used to verify the identity of the user so that the request can be signed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

