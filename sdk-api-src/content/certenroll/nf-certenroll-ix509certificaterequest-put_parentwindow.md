---
UID: NF:certenroll.IX509CertificateRequest.put_ParentWindow
title: IX509CertificateRequest::put_ParentWindow (certenroll.h)
description: Specifies and retrieves the ID of the window used by key-related user interface dialogs. (Put)
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","ParentWindow property","IX509CertificateRequest.ParentWindow","IX509CertificateRequest.put_ParentWindow","IX509CertificateRequest::ParentWindow","IX509CertificateRequest::get_ParentWindow","IX509CertificateRequest::put_ParentWindow","ParentWindow property [Security]","ParentWindow property [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::ParentWindow","certenroll/IX509CertificateRequest::get_ParentWindow","certenroll/IX509CertificateRequest::put_ParentWindow","put_ParentWindow","security.ix509certificaterequest_parentwindow_property"]
old-location: security\ix509certificaterequest_parentwindow_property.htm
tech.root: security
ms.assetid: 86e82a6c-7689-4bf3-8f64-e512040abd6a
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],ParentWindow property, IX509CertificateRequest.ParentWindow, IX509CertificateRequest.put_ParentWindow, IX509CertificateRequest::ParentWindow, IX509CertificateRequest::get_ParentWindow, IX509CertificateRequest::put_ParentWindow, ParentWindow property [Security], ParentWindow property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::ParentWindow, certenroll/IX509CertificateRequest::get_ParentWindow, certenroll/IX509CertificateRequest::put_ParentWindow, put_ParentWindow, security.ix509certificaterequest_parentwindow_property
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
 - IX509CertificateRequest::put_ParentWindow
 - certenroll/IX509CertificateRequest::put_ParentWindow
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
 - IX509CertificateRequest.ParentWindow
 - IX509CertificateRequest.get_ParentWindow
 - IX509CertificateRequest.put_ParentWindow
---

# IX509CertificateRequest::put_ParentWindow


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

You can set this property before calling any initialization method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method. If the certificate request contains nested requests and you set the <b>ParentWindow</b> property on the top level request, it is automatically propagated to all of the inner requests. You can, however, set the property manually on each of the inner objects.

For a PKCS #10 request, the property value is retrieved from and specified on the associated <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object if the key exists. For a PKCS #7 or CMC request the window ID is updated on the inner request and all signing certificates.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
