---
UID: NF:bcrypt.BCryptDeriveKey
title: BCryptDeriveKey function (bcrypt.h)
description: Derives a key from a secret handle. (BCryptDeriveKey)
helpviewer_keywords: ["BCRYPT_KDF_HASH","BCRYPT_KDF_HMAC","BCRYPT_KDF_SP80056A_CONCAT","BCRYPT_KDF_TLS_PRF","BCryptDeriveKey","BCryptDeriveKey function [Security]","KDF_USE_SECRET_AS_HMAC_KEY_FLAG","bcrypt/BCryptDeriveKey","security.bcryptderivekey"]
old-location: security\bcryptderivekey.htm
tech.root: security
ms.assetid: 33c3cbf7-6c08-42ed-ac3f-feb71f3a9cbf
ms.date: 06/27/2025
ms.keywords: BCRYPT_KDF_HASH, BCRYPT_KDF_HMAC, BCRYPT_KDF_SP80056A_CONCAT, BCRYPT_KDF_TLS_PRF, BCryptDeriveKey, BCryptDeriveKey function [Security], KDF_USE_SECRET_AS_HMAC_KEY_FLAG, bcrypt/BCryptDeriveKey, security.bcryptderivekey
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptDeriveKey
 - bcrypt/BCryptDeriveKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptDeriveKey
---

# BCryptDeriveKey function

## -description

The **BCryptDeriveKey** function derives a key from a **BCRYPT_SECRET_HANDLE**. This is typically done as part of a secret agreement procedure.

For key derivation from a secret directly provided by the caller, see [BCryptKeyDerivation](nf-bcrypt-bcryptkeyderivation.md).

## -parameters

### -param hSharedSecret [in]

The secret handle to create the key from. This handle is obtained from the [BCryptSecretAgreement](nf-bcrypt-bcryptsecretagreement.md) function.

### -param pwszKDF [in]

A pointer to a null-terminated Unicode string that identifies the *key derivation function* (KDF) to use to derive the key. This can be one of the following strings.

#### BCRYPT_KDF_HASH (L"HASH")

Use the hash key derivation function. 

If the *cbDerivedKey* parameter is less than the size of the derived key, this function will only copy the specified number of bytes to the *pbDerivedKey* buffer. This is usually bad practice as it can significantly reduce the security strength of the resulting key.

If the *cbDerivedKey* parameter is greater than the size of the derived key, this function will copy the key to the *pbDerivedKey* buffer and set the variable pointed to by the *pcbResult* to the actual number of bytes copied.

The parameters identified by the *pParameterList* parameter either can or must contain the following parameters, as indicated by the Required or optional column.

| Parameter | Description | Required or optional |
|-----------|-------------|----------------------|
| **KDF_HASH_ALGORITHM** | A null-terminated Unicode string that identifies the hash algorithm to use. This can be one of the standard hash algorithm identifiers from [CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers) or the identifier for another registered hash algorithm.<br/><br/>If this parameter is not specified, the SHA1 hash algorithm is used. | Optional |
| **KDF_SECRET_PREPEND** | A value to add to the beginning of the message input to the hash function. For more information, see Remarks. | Optional |
| **KDF_SECRET_APPEND** | A value to add to the end of the message input to the hash function. For more information, see Remarks. | Optional |

The call to the KDF is made as shown in the following pseudocode.

``` syntax
KDF-Output = Hash(
    KDF-Prepend + 
    hSharedSecret + 
    KDF-Append)
```

#### BCRYPT_KDF_HMAC (L"HMAC")

Use the [Hash-Based Message Authentication Code](/windows/win32/SecGloss/h-gly) (HMAC) key derivation function. 

If the *cbDerivedKey* parameter is less than the size of the derived key, this function will only copy the specified number of bytes to the *pbDerivedKey* buffer. This is usually bad practice as it can significantly reduce the security strength of the resulting key.

If the *cbDerivedKey* parameter is greater than the size of the derived key, this function will copy the key to the *pbDerivedKey* buffer and set the variable pointed to by the *pcbResult* to the actual number of bytes copied.

The parameters identified by the *pParameterList* parameter either can or must contain the following parameters, as indicated by the Required or optional column.

| Parameter | Description | Required or optional |
|-----------|-------------|----------------------|
| **KDF_HASH_ALGORITHM** | A null-terminated Unicode string that identifies the hash algorithm to use. This can be one of the standard hash algorithm identifiers from [CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers) or the identifier for another registered hash algorithm.<br/><br/>If this parameter is not specified, the SHA1 hash algorithm is used. | Optional |
| **KDF_HMAC_KEY** | The key to use for the [pseudo-random function](/windows/win32/SecGloss/p-gly) (PRF). | Optional |
| **KDF_SECRET_PREPEND** | A value to add to the beginning of the message input to the hash function. For more information, see Remarks. | Optional |
| **KDF_SECRET_APPEND** | A value to add to the end of the message input to the hash function. For more information, see Remarks. | Optional |

The call to the KDF is made as shown in the following pseudocode.

``` syntax
KDF-Output = HMAC-Hash(
    KDF_HMAC_KEY,
    KDF-Prepend + 
    hSharedSecret + 
    KDF-Append)
```

#### BCRYPT_KDF_TLS_PRF (L"TLS_PRF")

Use the [transport layer security](/windows/win32/SecGloss/t-gly) (TLS) [pseudo-random function](/windows/win32/SecGloss/p-gly) (PRF) key derivation function. The size of the derived key is always 48 bytes, so the *cbDerivedKey* parameter must be 48.

The parameters identified by the *pParameterList* parameter either can or must contain the following parameters, as indicated by the Required or optional column.

| Parameter | Description | Required or optional |
|-----------|-------------|----------------------|
| **KDF_TLS_PRF_LABEL** | An ANSI string that contains the PRF label. | Required |
| **KDF_TLS_PRF_SEED** | The PRF seed. The seed must be 64 bytes long. | Required |
| **KDF_TLS_PRF_PROTOCOL** | A **DWORD** value that specifies the TLS protocol version whose PRF algorithm is to be used.<br/><br/>Valid values are:<br/>SSL2_PROTOCOL_VERSION (0x0002)<br/>SSL3_PROTOCOL_VERSION (0x0300)<br/>TLS1_PROTOCOL_VERSION (0x0301)<br/>TLS1_0_PROTOCOL_VERSION (0x0301)<br/>TLS1_1_PROTOCOL_VERSION (0x0302)<br/>TLS1_2_PROTOCOL_VERSION (0x0303)<br/>DTLS1_0_PROTOCOL_VERSION (0xfeff)<br/><br/>**Windows Server 2008 and Windows Vista:** TLS1_1_PROTOCOL_VERSION, TLS1_2_PROTOCOL_VERSION and DTLS1_0_PROTOCOL_VERSION are not supported.<br/><br/>**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** DTLS1_0_PROTOCOL_VERSION is not supported. | Optional |
| **KDF_HASH_ALGORITHM** | The CNG algorithm ID of the hash to be used with the HMAC in the PRF, for the TLS 1.2 protocol version. Valid choices are SHA-256 and SHA-384. If not specified, SHA-256 is used. | Optional |

The call to the KDF is made as shown in the following pseudocode.

``` syntax
KDF-Output = PRF(
    hSharedSecret, 
    KDF_TLS_PRF_LABEL, 
    KDF_TLS_PRF_SEED)
```

#### BCRYPT_KDF_SP80056A_CONCAT (L"SP800_56A_CONCAT")

Use the SP800-56A key derivation function. This is also known as SP800-56C rev2 one-step KDF.

The KDF takes an approved hash function as a parameter, but this API chooses the hash function internally, matching the security strength of the hash algorithm to the algorithm used to generate the secret handle. (i.e. ECDH P-256 uses SHA256, ECDH P-384 uses SHA384)

The parameters identified by the *pParameterList* parameter either can or must contain the following parameters, as indicated by the Required or optional column. All parameter values are treated as opaque byte arrays.

| Parameter | Description | Required or optional |
|-----------|-------------|----------------------|
| **KDF_ALGORITHMID** | Specifies the **AlgorithmID** subfield of the **OtherInfo** field in the SP800-56A key derivation function. Indicates the intended purpose of the derived key. | Required |
| **KDF_PARTYUINFO** | Specifies the **PartyUInfo** subfield of the **OtherInfo** field in the SP800-56A key derivation function. The field contains public information contributed by the initiator. | Required |
| **KDF_PARTYVINFO** | Specifies the **PartyVInfo** subfield of the **OtherInfo** field in the SP800-56A key derivation function. The field contains public information contributed by the responder. | Required |
| **KDF_SUPPPUBINFO** | Specifies the **SuppPubInfo** subfield of the **OtherInfo** field in the SP800-56A key derivation function. The field contains public information known to both initiator and responder. | Optional |
| **KDF_SUPPPRIVINFO** | Specifies the **SuppPrivInfo** subfield of the **OtherInfo** field in the SP800-56A key derivation function. It contains private information known to both initiator and responder, such as a shared secret. | Optional |

The call to the KDF is made as shown in the following pseudocode.

``` syntax
KDF-Output = SP_800-56A_KDF(
    hSharedSecret,
    KDF_ALGORITHMID,
    KDF_PARTYUINFO,
    KDF_PARTYVINFO,
    KDF_SUPPPUBINFO,
    KDF_SUPPPRIVINFO)
```

**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.

#### BCRYPT_KDF_RAW_SECRET (L"TRUNCATE")

Returns the little-endian representation of the raw secret without any modification. Use of this option is usually bad practice, but may be required if you need to interoperate with an unsupported KDF.

If the *cbDerivedKey* parameter is less than the size of the derived key, this function will only copy the specified number of bytes to the *pbDerivedKey* buffer. This is usually bad practice as it can significantly reduce the security strength of the resulting key.

If the *cbDerivedKey* parameter is greater than the size of the derived key, this function will copy the key to the *pbDerivedKey* buffer and set the variable pointed to by the *pcbResult* to the actual number of bytes copied.

**Windows 8, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.


#### BCRYPT_KDF_HKDF (L"HKDF")

Use the HKDF (HMAC-based Extract-and-Expand KDF) function from RFC 5869.

In HKDF, a distinction is made between deriving a key from either:
1) The output of a secret agreement function, which is not uniformly random, and is considered to be input keying material (IKM). Almost all users of *BCryptDeriveKey* will have a secret handle of this form.
2) A uniformly random secret value.

##### The first step is to "Extract" a pseudorandom key (PRK) from the secret handle.

This step is performed by calling [BCryptSetProperty](nf-bcrypt-bcryptsetproperty.md) on a secret handle with **BCRYPT_HKDF_HASH_ALGORITHM** to set the hash algorithm to use in HMAC computations in HKDF.
This is followed by a second call to [BCryptSetProperty](nf-bcrypt-bcryptsetproperty.md) with one of either:
1) If the secret handle represents IKM, use **BCRYPT_HKDF_SALT_AND_FINALIZE** to provide the optional salt value and extract the PRK from the IKM and finalize the secret handle.
2) Otherwise, use **BCRYPT_HKDF_PRK_AND_FINALIZE** to directly transform the secret value into the HKDF PRK and finalize the secret handle.

##### The second step is to "Expand" the PRK into an output derived key.
This step is performed by calling *BCryptDeriveKey* on a finalized secret handle.

The parameters identified by the *pParameterList* parameter either can or must contain the following parameters, as indicated by the Required or optional column. All parameter values are treated as opaque byte arrays.

| Parameter | Description | Required or optional |
|-----------|-------------|----------------------|
| **KDF_HKDF_INFO** | Specifies the **info** field in the HKDF Expand Step. Indicates the optional context and application specific information. | Optional |

The call to the KDF is made as shown in the following pseudocode.


``` syntax
KDF-Output = HKDF-Expand(
    hSharedSecret.PRK,
    info,
    cbDerivedKey)
```

**Windows 10:** Support for HKDF begins.

### -param pParameterList [in, optional]

The address of a [BCryptBufferDesc](ns-bcrypt-bcryptbufferdesc.md) structure that contains the KDF parameters. This parameter is optional and can be `NULL` if it is not needed.

### -param pbDerivedKey [out, optional]

The address of a buffer that receives the key. The *cbDerivedKey* parameter contains the size of this buffer. If this parameter is `NULL`, this function will place the required size, in bytes, in the **ULONG** pointed to by the *pcbResult* parameter.

### -param cbDerivedKey [in]

The size, in bytes, of the *pbDerivedKey* buffer.

### -param pcbResult [out]

A pointer to a **ULONG** that receives the number of bytes that were copied to the *pbDerivedKey* buffer. If the *pbDerivedKey* parameter is `NULL`, this function will place the required size, in bytes, in the **ULONG** pointed to by this parameter.

### -param dwFlags [in]

A set of flags that modify the behavior of this function.

This can be zero or the following value:

| Value | Meaning |
| ----- | ------- |
| **KDF_USE_SECRET_AS_HMAC_KEY_FLAG** | The value in *hSharedSecret* will also serve as the HMAC key. If this flag is specified, the **KDF_HMAC_KEY** parameter should not be included in the set of parameters in the *pParameterList* parameter. This flag is only used by the **BCRYPT_KDF_HMAC** key derivation function. |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INTERNAL_ERROR** | An internal error occurred. |
| **STATUS_INVALID_HANDLE** | The handle in the *hSharedSecret* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |

## -remarks

The [BCryptBufferDesc](ns-bcrypt-bcryptbufferdesc.md) structure in the *pParameterList* parameter can contain more than one of the **KDF_SECRET_PREPEND** and **KDF_SECRET_APPEND** parameters. If more than one of these parameters is specified, the parameter values are concatenated in the order in which they are contained in the array before the KDF is called. For example, assume the following parameter values are specified.


```cpp
BYTE abValue0[] = {0x01};
BYTE abValue1[] = {0x04, 0x05};
BYTE abValue2[] = {0x10, 0x11, 0x12};
BYTE abValue3[] = {0x20, 0x21, 0x22, 0x23};

Parameter[0].type = KDF_SECRET_APPEND
Parameter[0].value = abValue0;
Parameter[0].length = sizeof (abValue0);
Parameter[1].type = KDF_SECRET_PREPEND
Parameter[1].value = abValue1;
Parameter[1].length = sizeof (abValue1);
Parameter[2].type = KDF_SECRET_APPEND
Parameter[2].value = abValue2;
Parameter[2].length = sizeof (abValue2);
Parameter[3].type = KDF_SECRET_PREPEND
Parameter[3].value = abValue3;
Parameter[3].length = sizeof (abValue3);

```


If the above parameter values are specified, the concatenated values to the actual KDF are as follows.


``` syntax
Type: KDF_SECRET_PREPEND
Value: {0x04, 0x05, 0x20, 0x21, 0x22, 0x23}, length 6

Type: KDF_SECRET_APPEND
Value: {0x01, 0x10, 0x11, 0x12}, length 4

```

If the *pwszKDF* parameter is set to **BCRYPT_KDF_RAW_SECRET**, the returned secret (unlike the other *pwszKDF* values) will be encoded in little-endian format. It is important to take note of this when using the raw secret in any other CNG functions, as most of them take in big-endian encoded inputs.


When using a supported algorithm provider, *BCryptDeriveKey* can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hSharedSecret* parameter must be located in nonpaged (or locked) memory and must be derived from an algorithm handle returned by a provider that was opened by using the **BCRYPT_PROV_DISPATCH** flag.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use Ksecdd.lib.

## -see-also

[BCryptBufferDesc](ns-bcrypt-bcryptbufferdesc.md)

[BCryptSecretAgreement](nf-bcrypt-bcryptsecretagreement.md)
