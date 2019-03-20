---
UID: NS:wincrypt._CERT_HASHED_URL
title: CERT_HASHED_URL (wincrypt.h)
author: windows-sdk-content
description: Contains a hashed URL.
old-location: security\cert_hashed_url.htm
tech.root: SecCrypto
ms.assetid: 961feb88-b924-4834-bc68-d87f410259f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_HASHED_URL, CERT_HASHED_URL, CERT_HASHED_URL structure [Security], PCERT_HASHED_URL, PCERT_HASHED_URL structure pointer [Security], security.cert_hashed_url, wincrypt/CERT_HASHED_URL, wincrypt/PCERT_HASHED_URL"
ms.topic: struct
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
---

# CERT_HASHED_URL structure


## -description


The <b>CERT_HASHED_URL</b> structure contains a hashed URL.


## -struct-fields




### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm used to create the URL hash.


### -field Hash

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains the hash value.


### -field pwszUrl

The address of a null-terminated Unicode string that contains the URL. This member is optional for biometric data and may be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/544297e2-b6a6-4a33-94b6-47066262506a">CERT_BIOMETRIC_DATA</a>



<a href="https://msdn.microsoft.com/cde420a8-c755-4c45-ab81-4897b08d9dd6">CERT_LOGOTYPE_DETAILS</a>



<a href="https://msdn.microsoft.com/22e6492e-afc2-4160-ad6c-0b65265eafeb">CERT_LOGOTYPE_REFERENCE</a>
 

 

