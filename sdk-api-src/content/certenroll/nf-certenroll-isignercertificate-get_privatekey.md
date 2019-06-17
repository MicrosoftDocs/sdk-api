---
UID: NF:certenroll.ISignerCertificate.get_PrivateKey
title: ISignerCertificate::get_PrivateKey (certenroll.h)
author: windows-sdk-content
description: Retrieves the private key associated with the ISignerCertificate object.
old-location: security\isignercertificate_privatekey_property.htm
tech.root: seccertenroll
ms.assetid: 047a22ba-9817-45b7-aa9a-356245d2b824
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],PrivateKey property, ISignerCertificate.PrivateKey, ISignerCertificate.get_PrivateKey, ISignerCertificate::PrivateKey, ISignerCertificate::get_PrivateKey, PrivateKey property [Security], PrivateKey property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::PrivateKey, certenroll/ISignerCertificate::get_PrivateKey, get_PrivateKey, security.isignercertificate_privatekey_property
ms.topic: method
f1_keywords: ["certenroll/ISignerCertificate.PrivateKey"]
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
 - ISignerCertificate.PrivateKey
 - ISignerCertificate.get_PrivateKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::get_PrivateKey


## -description


The <b>PrivateKey</b> property retrieves the private key associated with the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object.

This property is read-only.


## -parameters


## -remarks



When you call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated private key. You can also call the following properties to retrieve information about the signing certificate object:<ul>
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_silent">Silent</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
 

 

