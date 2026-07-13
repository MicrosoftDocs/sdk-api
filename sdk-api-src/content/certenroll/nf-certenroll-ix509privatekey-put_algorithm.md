---
UID: NF:certenroll.IX509PrivateKey.put_Algorithm
title: IX509PrivateKey::put_Algorithm (certenroll.h)
description: Specifies or retrieves an object identifier (OID) for the public key algorithm. (Put)
helpviewer_keywords: ["Algorithm property [Security]","Algorithm property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","Algorithm property","IX509PrivateKey.Algorithm","IX509PrivateKey.put_Algorithm","IX509PrivateKey::Algorithm","IX509PrivateKey::get_Algorithm","IX509PrivateKey::put_Algorithm","certenroll/IX509PrivateKey::Algorithm","certenroll/IX509PrivateKey::get_Algorithm","certenroll/IX509PrivateKey::put_Algorithm","put_Algorithm","security.ix509privatekey_algorithm"]
old-location: security\ix509privatekey_algorithm.htm
tech.root: security
ms.assetid: 40d2eae1-733a-4e5b-bb15-71301d73f438
ms.date: 12/05/2018
ms.keywords: Algorithm property [Security], Algorithm property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Algorithm property, IX509PrivateKey.Algorithm, IX509PrivateKey.put_Algorithm, IX509PrivateKey::Algorithm, IX509PrivateKey::get_Algorithm, IX509PrivateKey::put_Algorithm, certenroll/IX509PrivateKey::Algorithm, certenroll/IX509PrivateKey::get_Algorithm, certenroll/IX509PrivateKey::put_Algorithm, put_Algorithm, security.ix509privatekey_algorithm
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
 - IX509PrivateKey::put_Algorithm
 - certenroll/IX509PrivateKey::put_Algorithm
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
 - IX509PrivateKey.Algorithm
 - IX509PrivateKey.get_Algorithm
 - IX509PrivateKey.put_Algorithm
---

# IX509PrivateKey::put_Algorithm


## -description

The <b>Algorithm</b> property specifies or retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the public key algorithm. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

This property is automatically set when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspstatus">CspStatus</a> property is called.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
