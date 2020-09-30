---
UID: NS:wincrypt._CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
title: CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO (wincrypt.h)
description: Contains the length, in bits, of the public key and the names of the signing and hashing algorithms used for strong signing.
helpviewer_keywords: ["*PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO","CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO","CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure [Security]","PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO","PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure pointer [Security]","security.crypt_verify_cert_sign_strong_properties_info","wincrypt/CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO","wincrypt/PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO"]
old-location: security\crypt_verify_cert_sign_strong_properties_info.htm
tech.root: security
ms.assetid: 7D68DE3D-B05D-4E06-9BA1-72E407E5FED2
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure [Security], PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure pointer [Security], security.crypt_verify_cert_sign_strong_properties_info, wincrypt/CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, wincrypt/PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO, *PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
 - wincrypt/_CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
 - PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
 - wincrypt/PCRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
 - CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
 - wincrypt/CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
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
 - CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO
---

# CRYPT_VERIFY_CERT_SIGN_STRONG_PROPERTIES_INFO structure


## -description

Contains the length, in bits, of the public key and the  names of the signing and hashing algorithms used for strong signing.

## -struct-fields

### -field CertSignHashCNGAlgPropData

The buffer contains a Unicode string that denotes the signing algorithm / hashing algorithm pair used, for example "RSA/SHA256".

### -field CertIssuerPubKeyBitLengthPropData

The buffer contains the length, in bits, of the asymmetric key used for signing.

## -remarks

This structure is returned by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifycertificatesignatureex">CryptVerifyCertificateSignatureEx</a> function when the <i>dwFlags</i> parameter is set to <b>CRYPT_VERIFY_CERT_SIGN_RETURN_STRONG_PROPERTIES_FLAG</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifycertificatesignatureex">CryptVerifyCertificateSignatureEx</a>