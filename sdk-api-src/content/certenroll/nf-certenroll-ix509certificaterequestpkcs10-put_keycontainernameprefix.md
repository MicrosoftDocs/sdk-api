---
UID: NF:certenroll.IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix
title: IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix (certenroll.h)
description: Specifies or retrieves a prefix used to create the container name for a new private key. (Put)
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","KeyContainerNamePrefix property","IX509CertificateRequestPkcs10.KeyContainerNamePrefix","IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix","IX509CertificateRequestPkcs10::KeyContainerNamePrefix","IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix","IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix","KeyContainerNamePrefix property [Security]","KeyContainerNamePrefix property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::KeyContainerNamePrefix","certenroll/IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix","certenroll/IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix","put_KeyContainerNamePrefix","security.ix509certificaterequestpkcs10_keycontainernameprefix_property"]
old-location: security\ix509certificaterequestpkcs10_keycontainernameprefix_property.htm
tech.root: security
ms.assetid: d4a99b08-5616-4c75-b99f-680f55288baa
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],KeyContainerNamePrefix property, IX509CertificateRequestPkcs10.KeyContainerNamePrefix, IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix, IX509CertificateRequestPkcs10::KeyContainerNamePrefix, IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, KeyContainerNamePrefix property [Security], KeyContainerNamePrefix property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, put_KeyContainerNamePrefix, security.ix509certificaterequestpkcs10_keycontainernameprefix_property
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
 - IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix
 - certenroll/IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix
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
 - IX509CertificateRequestPkcs10.KeyContainerNamePrefix
 - IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
 - IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix
---

# IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix


## -description

The <b>KeyContainerNamePrefix</b> property specifies or retrieves a prefix used to create the container name for a new private key.

This property is read/write.

## -parameters

## -remarks

Each CryptoAPI <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> or Cryptography API: Next Generation (CNG) key provider maintains a key container for the private key. To retrieve the name of a key container for an existing key, use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a> property of the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object.

A prefix can contain any string limited to the maximum length of the key container name and to legal container name characters. For example, if you do not call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a> property to specify a key container name, one is automatically created when the private key is created, and the prefix to the container name will be the string "lp". For another example, if you are creating a test harness and want to differentiate key containers by the programs that generated them, you can use the name of the executable as the prefix.

You must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method, and you must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
