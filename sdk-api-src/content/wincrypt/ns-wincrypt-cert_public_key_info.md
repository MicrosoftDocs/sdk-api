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
f1_keywords: 
 - "wincrypt/CERT_PUBLIC_KEY_INFO"
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
ms.custom: 19H1
---

# CERT_PUBLIC_KEY_INFO structure


## -description


The <b>CERT_PUBLIC_KEY_INFO</b> structure contains a public key and its algorithm.


## -struct-fields




### -field Algorithm


<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the public key algorithm type and associated additional parameters.


### -field PublicKey

BLOB containing an encoded public key.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_info">CERT_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_request_info">CERT_REQUEST_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcomparepublickeyinfo">CertComparePublicKeyInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex">CryptImportPublicKeyInfoEx</a>
 

 

