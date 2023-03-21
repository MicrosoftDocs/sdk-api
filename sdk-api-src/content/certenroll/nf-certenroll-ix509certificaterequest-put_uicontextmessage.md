---
UID: NF:certenroll.IX509CertificateRequest.put_UIContextMessage
title: IX509CertificateRequest::put_UIContextMessage (certenroll.h)
description: Specifies or retrieves a context string to display in the user interface. (Put)
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","UIContextMessage property","IX509CertificateRequest.UIContextMessage","IX509CertificateRequest.put_UIContextMessage","IX509CertificateRequest::UIContextMessage","IX509CertificateRequest::get_UIContextMessage","IX509CertificateRequest::put_UIContextMessage","UIContextMessage property [Security]","UIContextMessage property [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::UIContextMessage","certenroll/IX509CertificateRequest::get_UIContextMessage","certenroll/IX509CertificateRequest::put_UIContextMessage","put_UIContextMessage","security.ix509certificaterequest_uicontextmessage_property"]
old-location: security\ix509certificaterequest_uicontextmessage_property.htm
tech.root: security
ms.assetid: 0eedb520-06c3-4106-8593-1c5fb0829d5e
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],UIContextMessage property, IX509CertificateRequest.UIContextMessage, IX509CertificateRequest.put_UIContextMessage, IX509CertificateRequest::UIContextMessage, IX509CertificateRequest::get_UIContextMessage, IX509CertificateRequest::put_UIContextMessage, UIContextMessage property [Security], UIContextMessage property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::UIContextMessage, certenroll/IX509CertificateRequest::get_UIContextMessage, certenroll/IX509CertificateRequest::put_UIContextMessage, put_UIContextMessage, security.ix509certificaterequest_uicontextmessage_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequest::put_UIContextMessage
 - certenroll/IX509CertificateRequest::put_UIContextMessage
dev_langs:
 - c++
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
---

# IX509CertificateRequest::put_UIContextMessage


## -description

The <b>UIContextMessage</b> property specifies or retrieves a context string to display in the user interface.

This property is read/write.

## -parameters

## -remarks

You can set this property before calling any initialization method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method. For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the property value is updated on the inner request and all signing certificates.

The context string should include additional information about an action. For example, if the user interface instructs the user to enter a smartcard PIN, the context string can indicate that a PIN is used to verify the identity of the user so that the request can be signed.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
