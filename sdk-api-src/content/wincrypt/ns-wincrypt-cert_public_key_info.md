---
UID: NS:wincrypt._CERT_PUBLIC_KEY_INFO
title: CERT_PUBLIC_KEY_INFO (wincrypt.h)
description: Contains a public key and its algorithm.
helpviewer_keywords: ["*PCERT_PUBLIC_KEY_INFO","CERT_PUBLIC_KEY_INFO","CERT_PUBLIC_KEY_INFO structure [Security]","PCERT_PUBLIC_KEY_INFO","PCERT_PUBLIC_KEY_INFO structure pointer [Security]","_crypto2_cert_public_key_info","security.cert_public_key_info","wincrypt/CERT_PUBLIC_KEY_INFO","wincrypt/PCERT_PUBLIC_KEY_INFO"]
old-location: security\cert_public_key_info.htm
tech.root: security
ms.assetid: bab6c147-b7cd-408a-acac-90f05921e065
ms.date: 12/05/2018
ms.keywords: '*PCERT_PUBLIC_KEY_INFO, CERT_PUBLIC_KEY_INFO, CERT_PUBLIC_KEY_INFO structure [Security], PCERT_PUBLIC_KEY_INFO, PCERT_PUBLIC_KEY_INFO structure pointer [Security], _crypto2_cert_public_key_info, security.cert_public_key_info, wincrypt/CERT_PUBLIC_KEY_INFO, wincrypt/PCERT_PUBLIC_KEY_INFO'
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
req.typenames: CERT_PUBLIC_KEY_INFO, *PCERT_PUBLIC_KEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_PUBLIC_KEY_INFO
 - wincrypt/_CERT_PUBLIC_KEY_INFO
 - PCERT_PUBLIC_KEY_INFO
 - wincrypt/PCERT_PUBLIC_KEY_INFO
 - CERT_PUBLIC_KEY_INFO
 - wincrypt/CERT_PUBLIC_KEY_INFO
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
 - CERT_PUBLIC_KEY_INFO
---

# CERT_PUBLIC_KEY_INFO structure


## -description

The <b>CERT_PUBLIC_KEY_INFO</b> structure contains a public key and its algorithm.

## -struct-fields

### -field Algorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the public key algorithm type and associated additional parameters.

### -field PublicKey

BLOB containing an encoded public key.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcomparepublickeyinfo">CertComparePublicKeyInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex">CryptImportPublicKeyInfoEx</a>