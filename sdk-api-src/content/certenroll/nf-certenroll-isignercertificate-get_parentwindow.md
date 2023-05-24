---
UID: NF:certenroll.ISignerCertificate.get_ParentWindow
title: ISignerCertificate::get_ParentWindow (certenroll.h)
description: Specifies or retrieves the ID of the window used to display signing certificate information. (Get)
helpviewer_keywords: ["ISignerCertificate interface [Security]","ParentWindow property","ISignerCertificate.ParentWindow","ISignerCertificate.get_ParentWindow","ISignerCertificate::ParentWindow","ISignerCertificate::get_ParentWindow","ISignerCertificate::put_ParentWindow","ParentWindow property [Security]","ParentWindow property [Security]","ISignerCertificate interface","certenroll/ISignerCertificate::ParentWindow","certenroll/ISignerCertificate::get_ParentWindow","certenroll/ISignerCertificate::put_ParentWindow","get_ParentWindow","security.isignercertificate_parentwindow_property"]
old-location: security\isignercertificate_parentwindow_property.htm
tech.root: security
ms.assetid: a1749c92-11e4-4726-a355-ccdd245b4df8
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],ParentWindow property, ISignerCertificate.ParentWindow, ISignerCertificate.get_ParentWindow, ISignerCertificate::ParentWindow, ISignerCertificate::get_ParentWindow, ISignerCertificate::put_ParentWindow, ParentWindow property [Security], ParentWindow property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::ParentWindow, certenroll/ISignerCertificate::get_ParentWindow, certenroll/ISignerCertificate::put_ParentWindow, get_ParentWindow, security.isignercertificate_parentwindow_property
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
 - ISignerCertificate::get_ParentWindow
 - certenroll/ISignerCertificate::get_ParentWindow
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
 - ISignerCertificate.ParentWindow
 - ISignerCertificate.get_ParentWindow
 - ISignerCertificate.put_ParentWindow
---

# ISignerCertificate::get_ParentWindow


## -description

The <b>ParentWindow</b> property specifies or retrieves the ID of the window used to display signing certificate information.

This property is read/write.

## -parameters

## -remarks

Call this property to specify a window ID before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method. The <b>ParentWindow</b> property internally sets the window ID on the  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object. You can retrieve the private key object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a> property. You can call the following properties to retrieve additional information about the signing certificate object:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_certificate">Certificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-put_pin">Pin</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_signatureinformation">SignatureInformation</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_silent">Silent</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
