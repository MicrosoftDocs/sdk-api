---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_CryptAttributes
title: IX509CertificateRequestPkcs10::get_CryptAttributes (certenroll.h)
description: Retrieves an ICryptAttributes collection of optional certificate attributes. (IX509CertificateRequestPkcs10.get_CryptAttributes)
helpviewer_keywords: ["CryptAttributes property [Security]","CryptAttributes property [Security]","IX509CertificateRequestPkcs10 interface","IX509CertificateRequestPkcs10 interface [Security]","CryptAttributes property","IX509CertificateRequestPkcs10.CryptAttributes","IX509CertificateRequestPkcs10.get_CryptAttributes","IX509CertificateRequestPkcs10::CryptAttributes","IX509CertificateRequestPkcs10::get_CryptAttributes","certenroll/IX509CertificateRequestPkcs10::CryptAttributes","certenroll/IX509CertificateRequestPkcs10::get_CryptAttributes","get_CryptAttributes","security.ix509certificaterequestpkcs10_cryptattributes_property"]
old-location: security\ix509certificaterequestpkcs10_cryptattributes_property.htm
tech.root: security
ms.assetid: 078b6c55-8b56-4075-a8fa-b3230041ded0
ms.date: 12/05/2018
ms.keywords: CryptAttributes property [Security], CryptAttributes property [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],CryptAttributes property, IX509CertificateRequestPkcs10.CryptAttributes, IX509CertificateRequestPkcs10.get_CryptAttributes, IX509CertificateRequestPkcs10::CryptAttributes, IX509CertificateRequestPkcs10::get_CryptAttributes, certenroll/IX509CertificateRequestPkcs10::CryptAttributes, certenroll/IX509CertificateRequestPkcs10::get_CryptAttributes, get_CryptAttributes, security.ix509certificaterequestpkcs10_cryptattributes_property
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
 - IX509CertificateRequestPkcs10::get_CryptAttributes
 - certenroll/IX509CertificateRequestPkcs10::get_CryptAttributes
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
 - IX509CertificateRequestPkcs10.CryptAttributes
 - IX509CertificateRequestPkcs10.get_CryptAttributes
---

# IX509CertificateRequestPkcs10::get_CryptAttributes


## -description

The <b>CryptAttributes</b> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection of optional certificate attributes.

This property is read-only.

## -parameters

## -remarks

 You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:

<ul>
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
