---
UID: NE:schannel._eTlsAlgorithmUsage
title: eTlsAlgorithmUsage
ms.date: 11/4/2019
targetos: Windows
description: Specifies the algorithm being used to disable cryptographic settings.
tech.root: security
req.construct-type: enumeration
req.ddi-compliance: 
req.header: schannel.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 1809 [desktop apps only]
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - schannel.h
api_name:
 - _eTlsAlgorithmUsage
 - eTlsAlgorithmUsage
f1_keywords:
 - _eTlsAlgorithmUsage
 - schannel/_eTlsAlgorithmUsage
 - eTlsAlgorithmUsage
 - schannel/eTlsAlgorithmUsage
dev_langs:
 - c++
---

## -description

Specifies the algorithm being used to disable cryptographic settings.

## -enum-fields

### -field TlsParametersCngAlgUsageKeyExchange

Key exchange algorithm. (*e.g. RSA, ECDHE, DHE*)

### -field TlsParametersCngAlgUsageSignature

Signature algorithm. (*e.g. RSA, DSA, ECDSA*)

### -field TlsParametersCngAlgUsageCipher

Encryption algorithm. (*e.g. AES, DES, RC4*)

### -field TlsParametersCngAlgUsageDigest

Digest of cipher suite. (*e.g. SHA1, SHA256, SHA384*)

### -field TlsParametersCngAlgUsageCertSig

Signature and/or hash used to sign certificate. (*e.g. RSA, DSA, ECDSA, SHA1, SHA256*)

## -remarks

## -see-also

[CRYPTO_SETTINGS](ns-schannel-crypto_settings.md)

