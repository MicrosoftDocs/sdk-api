---
UID: NS:schannel._CRYPTO_SETTINGS
title: CRYPTO_SETTINGS
ms.date: 06/25/2024
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
 - _CRYPTO_SETTINGS
 - schannel/_CRYPTO_SETTINGS
 - PCRYPTO_SETTINGS
 - schannel/PCRYPTO_SETTINGS
 - CRYPTO_SETTINGS
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

The <a href="/windows/win32/seccng/cng-algorithm-identifiers">CNG algorithm identifier</a>.

Cryptographic settings are ignored if the specified algorithm is not used by a supported, enabled cipher suite or an available credential.

### -field cChainingModes

The count of entries in the rgstrChainingModes array.

Set to 0 if strCngAlgId does not have a chaining mode (*e.g. BCRYPT_SHA384_ALGORITHM*). It is an error to specify more than SCH_CRED_MAX_SUPPORTED_CHAINING_MODES.

### -field rgstrChainingModes

An array of <a href="/windows/win32/seccng/cng-property-identifiers">CNG chaining mode identifiers</a>.

Set to NULL if strCngAlgId does not have a chaining mode (*e.g. BCRYPT_SHA384_ALGORITHM*).

### -field dwMinBitLength

Minimum bit length for the specified CNG algorithm.

If 0, schannel uses system defaults. Set to 0 if the CNG algorithm implies bit length (*e.g. BCRYPT_ECDH_P521_ALGORITHM*).

### -field dwMaxBitLength

Maximum bit length for the specified CNG algorithm.

If 0, schannel uses system defaults. Set to 0 if the CNG algorithm implies bit length (e.g. BCRYPT_ECDH_P521_ALGORITHM).

## -remarks

The following constant distinguishes between the different RSA padding modes and can be specified in the `strCngAlgId` field. Either of these modes can be provided instead of the <a href="/windows/win32/seccng/cng-algorithm-identifiers">CNG algorithm identifier</a>.

```cpp
#define SCHANNEL_RSA_PSS_PADDING_ALGORITHM L"SCH_RSA_PSS_PAD"
#define SCHANNEL_RSA_PKCS_PADDING_ALGORITHM L"SCH_RSA_PKCS_PAD"
```

## -see-also

[SCH_CREDENTIALS](ns-schannel-sch_credentials.md)

[TLS_PARAMETERS](ns-schannel-tls_parameters.md)

[eTlsAlgorithmUsage](ne-schannel-etlsalgorithmusage.md)
