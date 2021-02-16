---
UID: NF:certenroll.IX509PublicKey.get_Algorithm
title: IX509PublicKey::get_Algorithm (certenroll.h)
description: Retrieves an object identifier (OID) for the public key algorithm.
helpviewer_keywords: ["Algorithm property [Security]","Algorithm property [Security]","IX509PublicKey interface","IX509PublicKey interface [Security]","Algorithm property","IX509PublicKey.Algorithm","IX509PublicKey.get_Algorithm","IX509PublicKey::Algorithm","IX509PublicKey::get_Algorithm","certenroll/IX509PublicKey::Algorithm","certenroll/IX509PublicKey::get_Algorithm","get_Algorithm","security.ix509publickey_algorithm_property"]
old-location: security\ix509publickey_algorithm_property.htm
tech.root: security
ms.assetid: 6c34323e-669e-434c-946f-65fe53456a11
ms.date: 12/05/2018
ms.keywords: Algorithm property [Security], Algorithm property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],Algorithm property, IX509PublicKey.Algorithm, IX509PublicKey.get_Algorithm, IX509PublicKey::Algorithm, IX509PublicKey::get_Algorithm, certenroll/IX509PublicKey::Algorithm, certenroll/IX509PublicKey::get_Algorithm, get_Algorithm, security.ix509publickey_algorithm_property
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
 - IX509PublicKey::get_Algorithm
 - certenroll/IX509PublicKey::get_Algorithm
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
 - IX509PublicKey.Algorithm
 - IX509PublicKey.get_Algorithm
---

# IX509PublicKey::get_Algorithm


## -description

The <b>Algorithm</b> property retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the public key algorithm.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initializefromencodedpublickeyinfo">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initialize">Initialize</a> method to initialize the public key object before calling this property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>