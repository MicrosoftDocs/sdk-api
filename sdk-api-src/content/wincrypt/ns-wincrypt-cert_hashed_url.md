---
UID: NS:wincrypt._CERT_HASHED_URL
title: CERT_HASHED_URL (wincrypt.h)
description: Contains a hashed URL.
helpviewer_keywords: ["*PCERT_HASHED_URL","CERT_HASHED_URL","CERT_HASHED_URL structure [Security]","PCERT_HASHED_URL","PCERT_HASHED_URL structure pointer [Security]","security.cert_hashed_url","wincrypt/CERT_HASHED_URL","wincrypt/PCERT_HASHED_URL"]
old-location: security\cert_hashed_url.htm
tech.root: security
ms.assetid: 961feb88-b924-4834-bc68-d87f410259f1
ms.date: 12/05/2018
ms.keywords: '*PCERT_HASHED_URL, CERT_HASHED_URL, CERT_HASHED_URL structure [Security], PCERT_HASHED_URL, PCERT_HASHED_URL structure pointer [Security], security.cert_hashed_url, wincrypt/CERT_HASHED_URL, wincrypt/PCERT_HASHED_URL'
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
req.typenames: CERT_HASHED_URL, *PCERT_HASHED_URL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_HASHED_URL
 - wincrypt/_CERT_HASHED_URL
 - PCERT_HASHED_URL
 - wincrypt/PCERT_HASHED_URL
 - CERT_HASHED_URL
 - wincrypt/CERT_HASHED_URL
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
 - CERT_HASHED_URL
---

# CERT_HASHED_URL structure


## -description

The <b>CERT_HASHED_URL</b> structure contains a hashed URL.

## -struct-fields

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm used to create the URL hash.

### -field Hash

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the hash value.

### -field pwszUrl

The address of a null-terminated Unicode string that contains the URL. This member is optional for biometric data and may be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_biometric_data">CERT_BIOMETRIC_DATA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_details">CERT_LOGOTYPE_DETAILS</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_reference">CERT_LOGOTYPE_REFERENCE</a>