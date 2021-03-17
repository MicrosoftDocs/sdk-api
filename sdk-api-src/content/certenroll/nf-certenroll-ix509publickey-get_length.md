---
UID: NF:certenroll.IX509PublicKey.get_Length
title: IX509PublicKey::get_Length (certenroll.h)
description: Retrieves the length of the public key.
helpviewer_keywords: ["IX509PublicKey interface [Security]","Length property","IX509PublicKey.Length","IX509PublicKey.get_Length","IX509PublicKey::Length","IX509PublicKey::get_Length","Length property [Security]","Length property [Security]","IX509PublicKey interface","certenroll/IX509PublicKey::Length","certenroll/IX509PublicKey::get_Length","get_Length","security.ix509publickey_length_property"]
old-location: security\ix509publickey_length_property.htm
tech.root: security
ms.assetid: c386fb27-84c5-4570-9cdb-202baa726b96
ms.date: 12/05/2018
ms.keywords: IX509PublicKey interface [Security],Length property, IX509PublicKey.Length, IX509PublicKey.get_Length, IX509PublicKey::Length, IX509PublicKey::get_Length, Length property [Security], Length property [Security],IX509PublicKey interface, certenroll/IX509PublicKey::Length, certenroll/IX509PublicKey::get_Length, get_Length, security.ix509publickey_length_property
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
 - IX509PublicKey::get_Length
 - certenroll/IX509PublicKey::get_Length
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
 - IX509PublicKey.Length
 - IX509PublicKey.get_Length
---

# IX509PublicKey::get_Length


## -description

The <b>Length</b> property retrieves the length of the public key.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initializefromencodedpublickeyinfo">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initialize">Initialize</a> method to initialize the public key object before calling this property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>