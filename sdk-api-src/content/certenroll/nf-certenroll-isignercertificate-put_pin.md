---
UID: NF:certenroll.ISignerCertificate.put_Pin
title: ISignerCertificate::put_Pin (certenroll.h)
description: Specifies a personal identification number (PIN) used to authenticate a smart card user.
helpviewer_keywords: ["ISignerCertificate interface [Security]","Pin property","ISignerCertificate.Pin","ISignerCertificate.put_Pin","ISignerCertificate::Pin","ISignerCertificate::put_Pin","Pin property [Security]","Pin property [Security]","ISignerCertificate interface","certenroll/ISignerCertificate::Pin","certenroll/ISignerCertificate::put_Pin","put_Pin","security.isignercertificate_pin_property"]
old-location: security\isignercertificate_pin_property.htm
tech.root: security
ms.assetid: 695d895e-0646-4a2e-a699-86674f919bad
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],Pin property, ISignerCertificate.Pin, ISignerCertificate.put_Pin, ISignerCertificate::Pin, ISignerCertificate::put_Pin, Pin property [Security], Pin property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Pin, certenroll/ISignerCertificate::put_Pin, put_Pin, security.isignercertificate_pin_property
f1_keywords:
- certenroll/ISignerCertificate.Pin
dev_langs:
- c++
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
- ISignerCertificate.Pin
- ISignerCertificate.put_Pin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::put_Pin


## -description


The <b>Pin</b> property specifies a personal identification number (PIN) used to  authenticate a smart card user. A user must be authenticated before accessing the private key container on the smart card.

This property is write-only.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method. The <b>Pin</b> property internally sets the pin number on the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_certificate">Certificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_signatureinformation">SignatureInformation</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_silent">Silent</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
 

 

