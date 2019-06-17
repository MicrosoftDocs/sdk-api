---
UID: NS:wincrypt._CERT_HASHED_URL
title: CERT_HASHED_URL (wincrypt.h)
author: windows-sdk-content
description: Contains a hashed URL.
old-location: security\cert_hashed_url.htm
tech.root: SecCrypto
ms.assetid: 961feb88-b924-4834-bc68-d87f410259f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_HASHED_URL, CERT_HASHED_URL, CERT_HASHED_URL structure [Security], PCERT_HASHED_URL, PCERT_HASHED_URL structure pointer [Security], security.cert_hashed_url, wincrypt/CERT_HASHED_URL, wincrypt/PCERT_HASHED_URL"
ms.topic: struct
f1_keywords: ["wincrypt/CERT_HASHED_URL"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_HASHED_URL
product: Windows
targetos: Windows
req.typenames: CERT_HASHED_URL, *PCERT_HASHED_URL
req.redist: 
ms.custom: 19H1
---

# CERT_HASHED_URL structure


## -description


The <b>CERT_HASHED_URL</b> structure contains a hashed URL.


## -struct-fields




### -field HashAlgorithm

A <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm used to create the URL hash.


### -field Hash

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the hash value.


### -field pwszUrl

The address of a null-terminated Unicode string that contains the URL. This member is optional for biometric data and may be <b>NULL</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_biometric_data">CERT_BIOMETRIC_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_logotype_details">CERT_LOGOTYPE_DETAILS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_logotype_reference">CERT_LOGOTYPE_REFERENCE</a>
 

 

