---
UID: NS:wincrypt._CERT_PUBLIC_KEY_INFO
title: CERT_PUBLIC_KEY_INFO (wincrypt.h)
author: windows-sdk-content
description: Contains a public key and its algorithm.
old-location: security\cert_public_key_info.htm
tech.root: SecCrypto
ms.assetid: bab6c147-b7cd-408a-acac-90f05921e065
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_PUBLIC_KEY_INFO, CERT_PUBLIC_KEY_INFO, CERT_PUBLIC_KEY_INFO structure [Security], PCERT_PUBLIC_KEY_INFO, PCERT_PUBLIC_KEY_INFO structure pointer [Security], _crypto2_cert_public_key_info, security.cert_public_key_info, wincrypt/CERT_PUBLIC_KEY_INFO, wincrypt/PCERT_PUBLIC_KEY_INFO"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_PUBLIC_KEY_INFO
product: Windows
targetos: Windows
req.typenames: CERT_PUBLIC_KEY_INFO, *PCERT_PUBLIC_KEY_INFO
req.redist: 
---

# CERT_PUBLIC_KEY_INFO structure


## -description


The <b>CERT_PUBLIC_KEY_INFO</b> structure contains a public key and its algorithm.


## -struct-fields




### -field Algorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the public key algorithm type and associated additional parameters.


### -field PublicKey

BLOB containing an encoded public key.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>



<a href="https://msdn.microsoft.com/079e4d5e-c8cb-4c3e-8094-13b9a140d564">CertComparePublicKeyInfo</a>



<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="https://msdn.microsoft.com/d3a59f83-c761-46bb-ac4f-f42f689ea5f1">CryptImportPublicKeyInfoEx</a>
 

 

