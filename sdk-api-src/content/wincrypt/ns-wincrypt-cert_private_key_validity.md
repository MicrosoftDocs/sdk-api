---
UID: NS:wincrypt._CERT_PRIVATE_KEY_VALIDITY
title: CERT_PRIVATE_KEY_VALIDITY (wincrypt.h)
description: The CERT_PRIVATE_KEY_VALIDITY structure indicates a valid time span for the private key corresponding to a certificate's public key.
helpviewer_keywords: ["*PCERT_PRIVATE_KEY_VALIDITY","CERT_PRIVATE_KEY_VALIDITY","CERT_PRIVATE_KEY_VALIDITY structure [Security]","PCERT_PRIVATE_KEY_VALIDITY","PCERT_PRIVATE_KEY_VALIDITY structure pointer [Security]","_crypto2_cert_private_key_validity","security.cert_private_key_validity","wincrypt/CERT_PRIVATE_KEY_VALIDITY","wincrypt/PCERT_PRIVATE_KEY_VALIDITY"]
old-location: security\cert_private_key_validity.htm
tech.root: security
ms.assetid: 4764174f-eecc-402e-8395-d3e2be0b0ae6
ms.date: 12/05/2018
ms.keywords: '*PCERT_PRIVATE_KEY_VALIDITY, CERT_PRIVATE_KEY_VALIDITY, CERT_PRIVATE_KEY_VALIDITY structure [Security], PCERT_PRIVATE_KEY_VALIDITY, PCERT_PRIVATE_KEY_VALIDITY structure pointer [Security], _crypto2_cert_private_key_validity, security.cert_private_key_validity, wincrypt/CERT_PRIVATE_KEY_VALIDITY, wincrypt/PCERT_PRIVATE_KEY_VALIDITY'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CERT_PRIVATE_KEY_VALIDITY, *PCERT_PRIVATE_KEY_VALIDITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_PRIVATE_KEY_VALIDITY
 - wincrypt/_CERT_PRIVATE_KEY_VALIDITY
 - PCERT_PRIVATE_KEY_VALIDITY
 - wincrypt/PCERT_PRIVATE_KEY_VALIDITY
 - CERT_PRIVATE_KEY_VALIDITY
 - wincrypt/CERT_PRIVATE_KEY_VALIDITY
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
 - CERT_PRIVATE_KEY_VALIDITY
---

# CERT_PRIVATE_KEY_VALIDITY structure


## -description

The <b>CERT_PRIVATE_KEY_VALIDITY</b> structure indicates a valid time span for the private key corresponding to a certificate's public key. If the <b>NotBefore</b> component is zero or not present, no statement is made as to when the validity period of the private key begins. If the <b>NotAfter</b> component is zero or not present, no end date is set on the validity of the private key.

A <b>CERT_PRIVATE_KEY_VALIDITY</b> structure is a member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_attributes_info">CERT_KEY_ATTRIBUTES_INFO</a> structure.

## -struct-fields

### -field NotBefore

Date and time before which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized-time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotBefore</b> time is only precise to seconds.

### -field NotAfter

Date and time after which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotAfter</b> time is only precise to seconds.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_attributes_info">CERT_KEY_ATTRIBUTES_INFO</a>