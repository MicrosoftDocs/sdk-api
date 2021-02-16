---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_ReuseKey
title: IX509CertificateRequestPkcs10::get_ReuseKey (certenroll.h)
description: Retrieves a Boolean value that indicates whether an existing private key was used to sign the request.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","ReuseKey property","IX509CertificateRequestPkcs10.ReuseKey","IX509CertificateRequestPkcs10.get_ReuseKey","IX509CertificateRequestPkcs10::ReuseKey","IX509CertificateRequestPkcs10::get_ReuseKey","ReuseKey property [Security]","ReuseKey property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::ReuseKey","certenroll/IX509CertificateRequestPkcs10::get_ReuseKey","get_ReuseKey","security.ix509certificaterequestpkcs10_reusekey_property"]
old-location: security\ix509certificaterequestpkcs10_reusekey_property.htm
tech.root: security
ms.assetid: b6788885-1036-4edd-bbb9-4d9808771d95
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],ReuseKey property, IX509CertificateRequestPkcs10.ReuseKey, IX509CertificateRequestPkcs10.get_ReuseKey, IX509CertificateRequestPkcs10::ReuseKey, IX509CertificateRequestPkcs10::get_ReuseKey, ReuseKey property [Security], ReuseKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::ReuseKey, certenroll/IX509CertificateRequestPkcs10::get_ReuseKey, get_ReuseKey, security.ix509certificaterequestpkcs10_reusekey_property
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
 - IX509CertificateRequestPkcs10::get_ReuseKey
 - certenroll/IX509CertificateRequestPkcs10::get_ReuseKey
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
 - IX509CertificateRequestPkcs10.ReuseKey
 - IX509CertificateRequestPkcs10.get_ReuseKey
---

# IX509CertificateRequestPkcs10::get_ReuseKey


## -description

The <b>ReuseKey</b> property retrieves a Boolean value that indicates whether an existing private key was used to sign the request.

This property is read-only.

## -parameters

## -remarks

If you initialized the request object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a> method, you specified a value for the <i>InheritOptions</i> parameter that indicated whether the private key used to sign the request was inherited from the certificate. If you specified <b>InheritPrivateKey</b> for this parameter, the <b>ReuseKey</b> property returns a value of Boolean true.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>