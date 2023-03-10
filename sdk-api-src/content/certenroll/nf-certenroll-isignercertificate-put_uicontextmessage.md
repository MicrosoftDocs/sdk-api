---
UID: NF:certenroll.ISignerCertificate.put_UIContextMessage
title: ISignerCertificate::put_UIContextMessage (certenroll.h)
description: Specifies or retrieves a string that contains user interface text associated with the signing certificate. (Put)
helpviewer_keywords: ["ISignerCertificate interface [Security]","UIContextMessage property","ISignerCertificate.UIContextMessage","ISignerCertificate.put_UIContextMessage","ISignerCertificate::UIContextMessage","ISignerCertificate::get_UIContextMessage","ISignerCertificate::put_UIContextMessage","UIContextMessage property [Security]","UIContextMessage property [Security]","ISignerCertificate interface","certenroll/ISignerCertificate::UIContextMessage","certenroll/ISignerCertificate::get_UIContextMessage","certenroll/ISignerCertificate::put_UIContextMessage","put_UIContextMessage","security.isignercertificate_uicontextmessage_property"]
old-location: security\isignercertificate_uicontextmessage_property.htm
tech.root: security
ms.assetid: 0fd874b0-9093-4c1b-94a0-a2aaad19010e
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],UIContextMessage property, ISignerCertificate.UIContextMessage, ISignerCertificate.put_UIContextMessage, ISignerCertificate::UIContextMessage, ISignerCertificate::get_UIContextMessage, ISignerCertificate::put_UIContextMessage, UIContextMessage property [Security], UIContextMessage property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::UIContextMessage, certenroll/ISignerCertificate::get_UIContextMessage, certenroll/ISignerCertificate::put_UIContextMessage, put_UIContextMessage, security.isignercertificate_uicontextmessage_property
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
 - ISignerCertificate::put_UIContextMessage
 - certenroll/ISignerCertificate::put_UIContextMessage
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
 - ISignerCertificate.UIContextMessage
 - ISignerCertificate.get_UIContextMessage
 - ISignerCertificate.put_UIContextMessage
---

# ISignerCertificate::put_UIContextMessage


## -description

The <b>UIContextMessage</b> property specifies or retrieves a string that contains user interface text associated with the  signing certificate.

This property is read/write.

## -parameters

## -remarks

Call this property to specify a value before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method. You can also call the following properties to retrieve additional information about the signing certificate object:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_certificate">Certificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-put_pin">Pin</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_signatureinformation">SignatureInformation</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_silent">Silent</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
