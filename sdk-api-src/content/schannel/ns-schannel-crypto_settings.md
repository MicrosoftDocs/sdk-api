---
UID: NS:schannel._CRYPTO_SETTINGS
title: CRYPTO_SETTINGS
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Indicates disabled cryptographic settings.
tech.root: security
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: schannel.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 1809 [desktop apps only]
req.target-type: Windows
req.typenames: CRYPTO_SETTINGS, *PCRYPTO_SETTINGS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - schannel.h
api_name:
 - _CRYPTO_SETTINGS
 - CRYPTO_SETTINGS
f1_keywords:
 - schannel/_CRYPTO_SETTINGS
 - schannel/CRYPTO_SETTINGS
dev_langs:
 - c++
---

## -description
Indicates disabled cryptographic settings.

## -struct-fields

### -field eAlgorithmUsage
The algorithm being used as specified in the [eTlsAlgorithmUsage](ne-schannel-etlsalgorithmusage.md) enumeration.

|Value|Algorithm|
|--|--|
|TlsParametersCngAlgUsageKeyExchange |Key exchange algorithm. <br>(*e.g. RSA, ECDHE, DHE*) |
|TlsParametersCngAlgUsageSignature   |Signature algorithm. <br>(*e.g. RSA, DSA, ECDSA*)|
|TlsParametersCngAlgUsageCipher      |Encryption algorithm. <br>(*e.g. AES, DES, RC4*)|
|TlsParametersCngAlgUsageDigest      |Digest of cipher suite. <br> (*e.g. SHA1, SHA256, SHA384*)|
|TlsParametersCngAlgUsageCertSig     |Signature and/or hash used to sign certificate. <br>(*e.g. RSA, DSA, ECDSA, SHA1, SHA256*)|


### -field strCngAlgId
The <a href="https://docs.microsoft.com/windows/win32/seccng/cng-algorithm-identifiers?redirectedfrom=MSDN">CNG algorithm identifier</a>.

Cryptographic settings are ignored if the specified algorithm is not used by a supported, enabled cipher suite or an available credential.

### -field cChainingModes
The count of entries in the rgstrChainingModes array. 

Set to 0 if strCngAlgId does not have a chaining mode (*e.g. BCRYPT_SHA384_ALGORITHM*). It is an error to specify more than SCH_CRED_MAX_SUPPORTED_CHAINING_MODES.

### -field rgstrChainingModes
An array of <a href="https://msdn.microsoft.com/library/windows/desktop/aa376211(v=vs.85).aspx">CNG chaining mode identifiers</a>. 

Set to NULL if strCngAlgId does not have a chaining mode (*e.g. BCRYPT_SHA384_ALGORITHM*).

### -field dwMinBitLength
Minimum bit length for the specified CNG algorithm. 

If 0, schannel uses system defaults. Set to 0 if the CNG algorithm implies bit length (*e.g. BCRYPT_ECDH_P521_ALGORITHM*).

### -field dwMaxBitLength
Maximum bit length for the specified CNG algorithm.

If 0, schannel uses system defaults. Set to 0 if the CNG algorithm implies bit length (e.g. BCRYPT_ECDH_P521_ALGORITHM).

## -remarks

## -see-also
[SCH_CREDENTIALS](ns-schannel-sch_credentials.md)

[TLS_PARAMETERS](ns-schannel-tls_parameters.md)

[eTlsAlgorithmUsage](ne-schannel-etlsalgorithmusage.md)
