---
UID: NN:certenroll.IX509AttributeCspProvider
title: IX509AttributeCspProvider (certenroll.h)
description: Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.
helpviewer_keywords: ["IX509AttributeCspProvider","IX509AttributeCspProvider interface [Security]","IX509AttributeCspProvider interface [Security]","described","certenroll/IX509AttributeCspProvider","security.ix509attributecspprovider"]
old-location: security\ix509attributecspprovider.htm
tech.root: security
ms.assetid: 08954c87-f63b-4e1a-91b4-3773e392999b
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider, IX509AttributeCspProvider interface [Security], IX509AttributeCspProvider interface [Security],described, certenroll/IX509AttributeCspProvider, security.ix509attributecspprovider
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
 - IX509AttributeCspProvider
 - certenroll/IX509AttributeCspProvider
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
 - IX509AttributeCspProvider
---

# IX509AttributeCspProvider interface


## -description

The <b>IX509AttributeCspProvider</b> interface represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate. Cryptographic providers and key containers are used to generate and store keys and perform encryption, signing, and hashing.

This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.

## -inheritance

The <b>IX509AttributeCspProvider</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeCspProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
