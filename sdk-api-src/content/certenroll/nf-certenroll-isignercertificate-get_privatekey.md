---
UID: NF:certenroll.ISignerCertificate.get_PrivateKey
title: ISignerCertificate::get_PrivateKey (certenroll.h)
description: Retrieves the private key associated with the ISignerCertificate object.
helpviewer_keywords: ["ISignerCertificate interface [Security]","PrivateKey property","ISignerCertificate.PrivateKey","ISignerCertificate.get_PrivateKey","ISignerCertificate::PrivateKey","ISignerCertificate::get_PrivateKey","PrivateKey property [Security]","PrivateKey property [Security]","ISignerCertificate interface","certenroll/ISignerCertificate::PrivateKey","certenroll/ISignerCertificate::get_PrivateKey","get_PrivateKey","security.isignercertificate_privatekey_property"]
old-location: security\isignercertificate_privatekey_property.htm
tech.root: security
ms.assetid: 047a22ba-9817-45b7-aa9a-356245d2b824
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],PrivateKey property, ISignerCertificate.PrivateKey, ISignerCertificate.get_PrivateKey, ISignerCertificate::PrivateKey, ISignerCertificate::get_PrivateKey, PrivateKey property [Security], PrivateKey property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::PrivateKey, certenroll/ISignerCertificate::get_PrivateKey, get_PrivateKey, security.isignercertificate_privatekey_property
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
 - ISignerCertificate::get_PrivateKey
 - certenroll/ISignerCertificate::get_PrivateKey
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
 - ISignerCertificate.PrivateKey
 - ISignerCertificate.get_PrivateKey
---

# ISignerCertificate::get_PrivateKey


## -description

The <b>PrivateKey</b> property retrieves the private key associated with the <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object.

This property is read-only.

## -parameters

## -remarks

When you call the <a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated private key. You can also call the following properties to retrieve information about the signing certificate object:<ul>
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