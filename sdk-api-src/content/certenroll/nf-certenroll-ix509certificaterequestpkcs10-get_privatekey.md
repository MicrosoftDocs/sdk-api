---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_PrivateKey
title: IX509CertificateRequestPkcs10::get_PrivateKey (certenroll.h)
author: windows-sdk-content
description: Retrieves an IX509PrivateKey object that contains the private key used to sign the certificate request.
old-location: security\ix509certificaterequestpkcs10_privatekey_property.htm
tech.root: seccertenroll
ms.assetid: 691e136f-1434-4b72-b571-e14ade4f2cf2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],PrivateKey property, IX509CertificateRequestPkcs10.PrivateKey, IX509CertificateRequestPkcs10.get_PrivateKey, IX509CertificateRequestPkcs10::PrivateKey, IX509CertificateRequestPkcs10::get_PrivateKey, PrivateKey property [Security], PrivateKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::PrivateKey, certenroll/IX509CertificateRequestPkcs10::get_PrivateKey, get_PrivateKey, security.ix509certificaterequestpkcs10_privatekey_property
ms.topic: method
f1_keywords: 
 - "certenroll/IX509CertificateRequestPkcs10.PrivateKey"
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
 - IX509CertificateRequestPkcs10.PrivateKey
 - IX509CertificateRequestPkcs10.get_PrivateKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestPkcs10::get_PrivateKey


## -description


The <b>PrivateKey</b> property retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object that contains the private key used to sign the certificate request. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



 You must initialize the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
 

 

