---
UID: NF:certenroll.ISignerCertificate.get_SignatureInformation
title: ISignerCertificate::get_SignatureInformation (certenroll.h)
description: Retrieves an IX509SignatureInformation object that contains information about the certificate signature.
old-location: security\isignercertificate_signatureinformation_property.htm
tech.root: seccertenroll
ms.assetid: e870e17f-42e4-4548-b876-f5e0556bff0e
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],SignatureInformation property, ISignerCertificate.SignatureInformation, ISignerCertificate.get_SignatureInformation, ISignerCertificate::SignatureInformation, ISignerCertificate::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::SignatureInformation, certenroll/ISignerCertificate::get_SignatureInformation, get_SignatureInformation, security.isignercertificate_signatureinformation_property
ms.topic: method
f1_keywords:
- certenroll/ISignerCertificate.SignatureInformation
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
- ISignerCertificate.SignatureInformation
- ISignerCertificate.get_SignatureInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object that contains information about the certificate signature.

This property is read-only.


## -parameters


## -remarks



When you call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method the Certificate Enrollment Control creates an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object. You can also call the following properties to retrieve information about the signing certificate object:<ul>
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a>
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
 

 

