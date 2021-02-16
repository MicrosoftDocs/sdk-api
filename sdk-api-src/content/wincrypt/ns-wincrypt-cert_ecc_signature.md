---
UID: NS:wincrypt._CERT_ECC_SIGNATURE
title: CERT_ECC_SIGNATURE (wincrypt.h)
description: Contains the r and s values for an Elliptic Curve Digital Signature Algorithm (ECDSA) signature.
helpviewer_keywords: ["*PCERT_ECC_SIGNATURE","CERT_ECC_SIGNATURE","CERT_ECC_SIGNATURE structure [Security]","PCERT_ECC_SIGNATURE","PCERT_ECC_SIGNATURE structure pointer [Security]","security.cert_ecc_signature","wincrypt/CERT_ECC_SIGNATURE","wincrypt/PCERT_ECC_SIGNATURE"]
old-location: security\cert_ecc_signature.htm
tech.root: security
ms.assetid: f341d839-c06d-40e9-a6ed-79a627918110
ms.date: 12/05/2018
ms.keywords: '*PCERT_ECC_SIGNATURE, CERT_ECC_SIGNATURE, CERT_ECC_SIGNATURE structure [Security], PCERT_ECC_SIGNATURE, PCERT_ECC_SIGNATURE structure pointer [Security], security.cert_ecc_signature, wincrypt/CERT_ECC_SIGNATURE, wincrypt/PCERT_ECC_SIGNATURE'
req.header: wincrypt.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CERT_ECC_SIGNATURE, *PCERT_ECC_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_ECC_SIGNATURE
 - wincrypt/_CERT_ECC_SIGNATURE
 - PCERT_ECC_SIGNATURE
 - wincrypt/PCERT_ECC_SIGNATURE
 - CERT_ECC_SIGNATURE
 - wincrypt/CERT_ECC_SIGNATURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_ECC_SIGNATURE
---

# CERT_ECC_SIGNATURE structure


## -description

The <b>CERT_ECC_SIGNATURE</b> structure contains the r and s values for an Elliptic Curve Digital Signature Algorithm (ECDSA) signature.

## -struct-fields

### -field r

The r value of the ECDSA signature. This value is in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> order.

### -field s

The s value of the ECDSA signature. This value is in little-endian order.

## -remarks

Before encoding, a leading zero byte will be inserted for the <b>r</b> and <b>s</b> members. After decoding, a leading zero byte will be removed from the <b>r</b> and <b>s</b> members if the leading zero is present.