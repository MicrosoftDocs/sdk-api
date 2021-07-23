---
UID: NN:certenroll.IX509PrivateKey
title: IX509PrivateKey (certenroll.h)
description: Represents an asymmetric private key that can be used for encryption, signing, and key agreement.
helpviewer_keywords: ["IX509PrivateKey","IX509PrivateKey interface [Security]","IX509PrivateKey interface [Security]","described","certenroll/IX509PrivateKey","security.ix509privatekey"]
old-location: security\ix509privatekey.htm
tech.root: security
ms.assetid: 72612ea4-ed45-46ac-9dad-614a9a754d83
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey, IX509PrivateKey interface [Security], IX509PrivateKey interface [Security],described, certenroll/IX509PrivateKey, security.ix509privatekey
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
 - IX509PrivateKey
 - certenroll/IX509PrivateKey
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
 - IX509PrivateKey
---

# IX509PrivateKey interface


## -description

The <b>IX509PrivateKey</b> interface represents an asymmetric private key that can be used for encryption, signing, and key agreement.  Private keys are referenced in the following objects:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</li>
</ul>

## -inheritance

The <b>IX509PrivateKey</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509PrivateKey</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>
