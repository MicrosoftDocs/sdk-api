---
UID: NF:ncrypt.NCryptCreateClaim
title: NCryptCreateClaim function (ncrypt.h)
description: Creates a key attestation claim.
helpviewer_keywords: ["NCryptCreateClaim","NCryptCreateClaim function [Security]","ncrypt/NCryptCreateClaim","security.ncryptcreateclaim"]
old-location: security\ncryptcreateclaim.htm
tech.root: security
ms.assetid: EBEE3A67-0693-4B85-88B1-580CB2152703
ms.date: 11/01/2024
ms.keywords: NCryptCreateClaim, NCryptCreateClaim function [Security], ncrypt/NCryptCreateClaim, security.ncryptcreateclaim
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptCreateClaim
 - ncrypt/NCryptCreateClaim
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ncrypt.dll
api_name:
 - NCryptCreateClaim
---

# NCryptCreateClaim function

## -description

Creates a key attestation claim.

## -parameters

### -param hSubjectKey [in]

The subject key handle that the claim is created for.

### -param hAuthorityKey [in, optional]

The authority key handle that the claim is based on.

### -param dwClaimType [in]

The type of claim.

### -param pParameterList [in, optional]

An optional parameter list.

### -param pbClaimBlob [out]

Output of the created claim blob.

### -param cbClaimBlob [in]

The size, in bytes, of the *pbClaimBlob* buffer.

### -param pcbResult [out]

The output of the created claim blob.

### -param dwFlags [in]

There are currently no flags defined. The *dwFlags* parameter should be set to `0`.

## -remarks

#### Protecting/attesting private keys using Virtualization Based Security (VBS)

> [!NOTE]
> Information regarding VBS flags relates to prerelease product that may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

This API helps enable an advanced attestation of security keys based on VBS key protection, a Windows module for protecting/attesting private keys using VBS. The attestation of a security key proves the association of this key to an anchored key, aka an attestation key. This capability may enhance the security level of communication between different entities by restricting the usage of out of context keys.

The API defines new flags to support creation and verification of attestation claims based on attestation keys in VBS key protection.

The following are *dwClaimType* types that are defined for the API:

| Claim Type | Description |
|------------|-------------|
| **NCRYPT_CLAIM_VBS_ROOT** | This type indicates that the generated claim is produced by the VBS root key. |
| **NCRYPT_CLAIM_VBS_IDENTITY** | This type indicates that the generated claim is produced by a VBS identity/attestation. This mean that the claim is produced by a VBS key that is elevated with the attestation flag **NCRYPT_ALLOW_KEY_ATTESTATION_FLAG** (see details below). |

The following are buffer types to be set in *pParameterList* buffer when creating an attestation claim:

> [!div class="mx-tdBreakAll"]
> | Buffer Type | Description |
> |-------------|-------------|
> | **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_HASH** | A buffer type to be set in a parameter buffer when creating an attestation claim in **NCryptCreateClaim**. This is a mandatory parameter type for **NCRYPT_CLAIM_VBS_IDENTITY** claims.<br/><br/>This parameter configures the type of hash function type to be used through the attestation claim creation. The values for this parameter are defined in `ncrypt.h` (like the constants in [CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers)):<br/><br/>`#define NCRYPT_SHA1_ALGORITHM BCRYPT_SHA1_ALGORITHM`<br/>`#define NCRYPT_SHA256_ALGORITHM BCRYPT_SHA256_ALGORITHM`<br/>`#define NCRYPT_SHA384_ALGORITHM BCRYPT_SHA384_ALGORITHM`<br/>`#define NCRYPT_SHA512_ALGORITHM BCRYPT_SHA512_ALGORITHM` |
> | **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_SCHEME** | A buffer type to be set in a parameter buffer when creating an attestation claim in **NCryptCreateClaim**. This is a mandatory parameter in case that the attestation key in the created **NCRYPT_CLAIM_VBS_IDENTITY** claim is an RSA key.<br/><br/>This parameter configures the padding scheme for the signature function type to be used through the attestation claim creation. The optional values for this parameter are defined in `bcrypt.h` (like the *dwFlags* constants in [NCryptSignHash](nf-ncrypt-ncryptsignhash.md)):<br/><br/>`#define BCRYPT_PAD_PSS 0x00000008` |
> | **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_ALGO** | A new buffer type to be set in a parameter buffer when creating an attestation claim in **NCryptCreateClaim**. This is a mandatory parameter in case that the attestation key in the created **NCRYPT_CLAIM_VBS_IDENTITY** claim is an RSA key. The parameter is a pointer to a null-terminated Unicode string that identifies the cryptographic algorithm to use to create the padding. This algorithm must be a hashing algorithm. The values for this parameter are defined in `ncrypt.h` (like the constants in [CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers)):<br/><br/>`#define NCRYPT_SHA1_ALGORITHM BCRYPT_SHA1_ALGORITHM`<br/>`#define NCRYPT_SHA256_ALGORITHM BCRYPT_SHA256_ALGORITHM`<br/>`#define NCRYPT_SHA384_ALGORITHM BCRYPT_SHA384_ALGORITHM`<br/>`#define NCRYPT_SHA512_ALGORITHM BCRYPT_SHA512_ALGORITHM` |
> | **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_SALT_SIZE** | A new buffer type to be set in a parameter buffer when creating an attestation claim in **NCryptCreateClaim**. This is a mandatory parameter in case that the attestation key in the created **NCRYPT_CLAIM_VBS_IDENTITY** claim is an RSA key.<br/><br/>The parameter represents a size, in bytes, of the random salt to use for the padding. |
> | **NCRYPTBUFFER_ATTESTATION_STATEMENT_NONCE** | A buffer type to be set in a parameter buffer when when creating an attestation claim in **NCryptCreateClaim**. This parameter is an alias to **NCRYPTBUFFER_CLAIM_KEYATTESTATION_NONCE**. |

#### Examples

This example illustrates the usage of the new API flag **NCRYPT_ALLOW_KEY_ATTESTATION_FLAG**. In addition, the nonce value for the claim creation is set by the **NCRYPTBUFFER_ATTESTATION_STATEMENT_NONCE** parameter type.

The example consists of these main steps:

1. A new attestation key is created. The key is specialized using the API function [NCryptSetProperty](nf-ncrypt-ncryptsetproperty.md). The generation of an attestation is based on a signing key.
1. A claim is created for further attestation. The claim is associated with the attestation key and with a built-in VBS key. The claim may be verified in [NCryptVerifyClaim](nf-ncrypt-ncryptverifyclaim.md) by providing the attestation key.
1. The attestation key object is freed to avoid memory leak.

```c
// Create an attestation/identity key. This function is invoked in the main code flow below.
NCRYPT_KEY_HANDLE CreateAttestationKey(NCRYPT_PROV_HANDLE provider)
{

    NCRYPT_KEY_HANDLE attestationKey = NULL;
    HRESULT hr;

    if (FAILED(hr = NCryptCreatePersistedKey(
                    provider,
                    &attestationKey,
                    BCRYPT_RSA_ALGORITHM,
                    L"AttestationKey", // a unique name for the attestation key in the key store
                    0, //dwLegacyKeySpec, not used
                    NCRYPT_REQUIRE_VBS_FLAG/*This flag targets VBS */)))
    {
        wprintf(L"Error creating an Attestation Identity Key with NCryptCreatePersistedKey(): 0x%X\n", hr);
        goto cleanup;
    }

    // This is a new flag. It’s used to enable the capability in an attestation key.
    DWORD keyUsagePolicy = NCRYPT_ALLOW_KEY_ATTESTATION_FLAG;
    if (FAILED(hr = NCryptSetProperty(
                    attestationKey,
                    NCRYPT_KEY_USAGE_PROPERTY,
                    (PUCHAR)&keyUsagePolicy,
                    sizeof(keyUsagePolicy),
                    0 /*dwFlags*/)))
    {
        wprintf(L"Error setting property with NCryptSetProperty (): 0x%X\n", hr);
        goto cleanup;
    }

    DWORD keySizeBits = 2048; // minimum allowed RSA key size
    if (FAILED(hr = NCryptSetProperty(
                    attestationKey,
                    NCRYPT_LENGTH_PROPERTY,
                    (PUCHAR)&keySizeBits,
                    sizeof(keySizeBits),
                    0 /*dwFlags*/)))
    {
        wprintf(L"Error setting property with NCryptSetProperty (): 0x%X\n", hr);
        goto cleanup;
    }
    
    if (FAILED(hr = NCryptFinalizeKey(attestationKey, 0 /*dwFlags*/)))
    {
        wprintf(L"Error finalizing key with NCryptFinalizeKey (): 0x%X\n", hr);
        goto cleanup;
    }

    return attestationKey;
cleanup:
    if (attestationKey != NULL)
    {
        NCryptFreeObject(attestationKey);
    }

    return NULL;
}

HRESULT CreateAttestation()
{
    HRESULT hr = S_OK;
    NCRYPT_PROV_HANDLE provider = NULL;
    
    BYTE nonce[] = "TheSuperSecretNonce";
    // This way of setting parameters is an existent pattern for NCrypt APIs
    NCryptBuffer paramBuffers[] =
    {
        { sizeof(nonce), NCRYPTBUFFER_ATTESTATION_STATEMENT_NONCE, (PBYTE)&nonce },
    };
    NCryptBufferDesc params = { NCRYPTBUFFER_VERSION, ARRAYSIZE(paramBuffers), paramBuffers };
    
    if (FAILED(hr = NCryptOpenStorageProvider(&provider, MS_KEY_STORAGE_PROVIDER, 0)))
    {
        wprintf(L"Error opening storage provider in NCryptOpenStorageProvider: 0x%X\n", hr);
        goto cleanup;
    }
    
    // Create a VBS attestation key
    NCRYPT_KEY_HANDLE attestationKey = CreateAttestationKey(provider);
    if (attestationKey == NULL)
    {
        hr = E_ABORT;
        goto cleanup;
    }
    
    DWORD bytesWritten = 0;
    
    if (FAILED(hr = NCryptCreateClaim(
                    attestationKey, // key that is being attested here and may attest other keys.
                    NULL, // implies that IDKS (VBS root signing key) will be used.
                    NCRYPT_CLAIM_VBS_ROOT, // used to attest a key with IDKS (VBS root signing key).
                    &params, // parameters list
                    NULL, // getting the size
                    0, // getting the size
                    &bytesWritten,
                    0 /*dwFlags*/)))
    {
        wprintf(L"Error creating claim with NCryptCreateClaim (): 0x%X\n", hr);
        goto cleanup;
    }
    
    DWORD claimBufferSize = bytesWritten;
    
    PBYTE claimBuffer = (PBYTE) HeapAlloc(GetProcessHeap(), 0,claimBufferSize);
    if (NULL == claimBuffer)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Error allocating buffer for the claim: 0x%X\n", hr);
        goto cleanup;
    }
    
    bytesWritten = 0;
    if (FAILED(hr = NCryptCreateClaim(
                    attestationKey, // key that is being attested here and may attest other keys.
                    NULL, //implies that IDKS (VBS root signing key) will be used.
                    NCRYPT_CLAIM_VBS_ROOT, // used to attest with IDKS (VBS root signing key).
                    &params, // parameters list
                    claimBuffer,
                    claimBufferSize,
                    &bytesWritten,
                    0)))
    {
        wprintf(L"Error creating claim with NCryptCreateClaim (): 0x%X\n", hr);
        goto cleanup;
    }
    
    wprintf(L"The claim is created successfully. It may be shared with the verifier side.\n");

cleanup:
    if (provider != NULL)
    {
        NCryptFreeObject(provider);
    }
    if (attestationKey != NULL)
    {
        NCryptFreeObject(attestationKey);
    }
    if (claimBuffer)
    {
        HeapFree(GetProcessHeap(), 0, claimBuffer);
    }
    
    return hr;
}
```

This next example illustrates the usage of new API parameters for creating a general-purpose cryptographic key and an associated attestation claim. This general-purpose key is used to generate an attestation claim.

The hash algorithm type and the padding for the claim creation are set in the **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_HASH** and **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_\[SCHEME/ALGO/SALT_SIZE\]** parameters respectively.

Please note that:

- The **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_HASH** parameter is mandatory only for **NCRYPT_CLAIM_VBS_IDENTITY** claims and meaningless in other types of claims.
- The **NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING** parameter is mandatory only for **NCRYPT_CLAIM_VBS_IDENTITY** claims in case of an RSA attestation key. In other types of claims it's meaningless.

The claim enables us to verify that the general-purpose key is associated with the attestation key.

```c
//
HRESULT hr = S_OK;
NCRYPT_PROV_HANDLE provider = NULL;

if (FAILED(hr = NCryptOpenStorageProvider(&provider, MS_KEY_STORAGE_PROVIDER, 0)))
{
    wprintf(L"Error opening storage provider in NCryptOpenStorageProvider: 0x%X\n", hr);
    goto cleanup;
}

NCRYPT_KEY_HANDLE attestationKey = NULL;

// Open the attestation key, created in CreateAttestationKey(), see previous example
if (FAILED(hr = NCryptOpenKey(
                provider,
                &attestationKey,
                L"AttestationKey",
                0, //dwLegacyKeySpec, not used
                0 ,/* dwFlags */)))
{
    wprintf(L"Error openning the attestation key with NCryptOpenKey (): 0x%X\n", hr);
    goto cleanup;
}

NCRYPT_KEY_HANDLE tokenKey = NULL; // Token key that is bound to the security token

// Create VBS token (general purpose) key
if (FAILED(hr = NCryptCreatePersistedKey(
                provider,
                &tokenKey,
                BCRYPT_RSA_ALGORITHM,
                L"TokenKey",
                0, //dwLegacyKeySpec, not used
                NCRYPT_REQUIRE_VBS_FLAG /*This flag targets VBS*/)))
{
    wprintf(L"Error creating an token key with NCryptCreatePersistedKey(): 0x%X\n", hr);
    goto cleanup;
}

DWORD keySizeBits = 2048;
if (FAILED(hr = NCryptSetProperty(
                tokenKey,
                NCRYPT_LENGTH_PROPERTY,
                (PUCHAR)&keySizeBits,
                sizeof(keySizeBits),
                0 /*dwFlags*/)))
{
    wprintf(L"Error setting property with NCryptSetProperty (): 0x%X\n", hr);
    goto cleanup;
}

if (FAILED(hr = NCryptFinalizeKey(tokenKey, 0 /*dwFlags*/)))
{
    wprintf(L"Error finalizing key with NCryptFinalizeKey (): 0x%X\n", hr);
    goto cleanup;
}

DWORD bytesWritten = 0;

DWORD hashAlgoType; // This is a new flag. It’s used to set type of hash algorithm of the claim// Set specific hash function type to produce the claim
wchar_t pHashAlgo[] = NCRYPT_SHA512_ALGORITHM;
// Set specific padding scheme for hash function to produce the claim
ULONG paddingScheme = BCRYPT_PAD_PSS;
wchar_t pPaddingAlgo[] = NCRYPT_SHA256_ALGORITHM;
ULONG paddingSalt = 345;

// This way of setting parameters is an existent pattern for NCrypt APIs
NCryptBuffer paramBuffers[] =
{
    { sizeof(NCRYPT_SHA512_ALGORITHM), NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_HASH, (PBYTE)&pHashAlgo },
    { sizeof(paddingScheme), NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_SCHEME , (PBYTE)&paddingScheme },
    { sizeof(NCRYPT_SHA256_ALGORITHM), NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_ALGO, (PBYTE)&pPaddingAlgo },
    { sizeof(paddingSalt, NCRYPTBUFFER_ATTESTATION_STATEMENT_SIGNATURE_PADDING_SALT_SIZE, (PBYTE)&paddingSalt }
};
NCryptBufferDesc params = { NCRYPTBUFFER_VERSION, ARRAYSIZE(paramBuffers), paramBuffers };

if (FAILED(hr = NCryptCreateClaim(
                tokenKey, // key that is being attested
                attestationKey,
                NCRYPT_CLAIM_VBS_IDENTITY, // attest general-purpose key with an attestation (identity) key.
                &params, // parameters list
                NULL, // getting the size
                0, // getting the size
                &bytesWritten,
                0 /*dwFlags*/)))
{
    wprintf(L"Error creating claim with NCryptCreateClaim (): 0x%X\n", hr);
    goto cleanup;
}

DWORD claimBufferSize = bytesWritten;

PBYTE claimBuffer = (PBYTE) HeapAlloc(GetProcessHeap(), 0,claimBufferSize);
if (NULL == claimBuffer)
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    wprintf(L"Error allocating buffer for the claim: 0x%X\n", hr);
    goto cleanup;
}
bytesWritten = 0;

if (FAILED(hr = NCryptCreateClaim(
                tokenKey, // key that is being attested
                attestationKey, // we assume that it is already initialized
                NCRYPT_CLAIM_VBS_IDENTITY, // attest general-purpose key with an attestation (identity) key
                &params,
                claimBuffer,
                claimBufferSize,
                &bytesWritten,
                0)))
{
    wprintf(L"Error creating claim with NCryptCreateClaim (): 0x%X\n", hr);
    goto cleanup;
}

wprintf(L"The claim is created successfully. It may be shared with the verifier side.\n");

cleanup:
    if (provider != NULL)
    {
    NCryptFreeObject(provider);
    }
    if (tokenKey != NULL)
    {
    NCryptFreeObject(tokenKey);
    }
    if (attestationKey != NULL)
    {
    NCryptDeleteKey(attestationKey);
    }
    if (claimBuffer)
    {
    HeapFree(GetProcessHeap(), 0, claimBuffer);
    }
    
return hr;
```

## -returns

Returns a status code that indicates the success or failure of the function.
