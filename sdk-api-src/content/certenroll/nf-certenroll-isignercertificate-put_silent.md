---
UID: NF:certenroll.ISignerCertificate.put_Silent
title: ISignerCertificate::put_Silent (certenroll.h)
description: Specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.
helpviewer_keywords: ["ISignerCertificate interface [Security]","Silent property","ISignerCertificate.Silent","ISignerCertificate.put_Silent","ISignerCertificate::Silent","ISignerCertificate::get_Silent","ISignerCertificate::put_Silent","Silent property [Security]","Silent property [Security]","ISignerCertificate interface","certenroll/ISignerCertificate::Silent","certenroll/ISignerCertificate::get_Silent","certenroll/ISignerCertificate::put_Silent","put_Silent","security.isignercertificate_silent_property"]
old-location: security\isignercertificate_silent_property.htm
tech.root: security
ms.assetid: b598d4a2-d53a-4091-a059-f9674acf9318
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],Silent property, ISignerCertificate.Silent, ISignerCertificate.put_Silent, ISignerCertificate::Silent, ISignerCertificate::get_Silent, ISignerCertificate::put_Silent, Silent property [Security], Silent property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Silent, certenroll/ISignerCertificate::get_Silent, certenroll/ISignerCertificate::put_Silent, put_Silent, security.isignercertificate_silent_property
f1_keywords:
- certenroll/ISignerCertificate.Silent
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
- ISignerCertificate.Silent
- ISignerCertificate.get_Silent
- ISignerCertificate.put_Silent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::put_Silent


## -description


The <b>Silent</b> property specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method. Setting this property also sets the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_silent">Silent</a> property on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_certificate">Certificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-put_pin">Pin</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_signatureinformation">SignatureInformation</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
 

 

