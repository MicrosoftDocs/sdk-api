---
UID: NF:ncrypt.NCryptVerifyClaim
title: NCryptVerifyClaim function (ncrypt.h)
description: Verifies a key attestation claim.
helpviewer_keywords: ["NCryptVerifyClaim","NCryptVerifyClaim function [Security]","ncrypt/NCryptVerifyClaim","security.ncryptverifyclaim"]
old-location: security\ncryptverifyclaim.htm
tech.root: security
ms.assetid: D3C837A5-49D7-4099-B8FE-37364A275A73
ms.date: 11/01/2024
ms.keywords: NCryptVerifyClaim, NCryptVerifyClaim function [Security], ncrypt/NCryptVerifyClaim, security.ncryptverifyclaim
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
 - NCryptVerifyClaim
 - ncrypt/NCryptVerifyClaim
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
 - NCryptVerifyClaim
---

# NCryptVerifyClaim function

## -description

Verifies a key attestation claim.

## -parameters

### -param hSubjectKey [in]

The subject key handle for the claim.

### -param hAuthorityKey [in, optional]

The authority key handle to use when verifying the claim. This parameter is optional because the authority key is self-contained for certain claim types.

### -param dwClaimType [in]

The type of claim.

### -param pParameterList [in, optional]

An optional parameter list.

### -param pbClaimBlob [in]

The input claim blob.

### -param cbClaimBlob [in]

The size, in bytes, of the *pbClaimBlob* buffer.

### -param pOutput [out]

The output blob.

### -param dwFlags [in]

**NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG** is a new flag to be set during verification of a VBS-generated claim. See the [remarks](#-remarks) section for more information.

There are currently no other flags defined. The *dwFlags* parameter should be set to `0` for all other verification types.

## -remarks

#### Protecting/attesting private keys using Virtualization Based Security (VBS)

> [!NOTE]
> Information regarding VBS flags relates to prerelease product that may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

This API helps enable an advanced attestation of security keys based on VBS key protection, a Windows module for protecting and attesting private keys using VBS. The attestation of a security key proves the association of this key to an anchored key, aka an attestation key. This capability may enhance the security level of communication between different entities by restricting the usage of out of context keys.

The API defines new flags to support creation and verification of attestation claims based on attestation keys in VBS key protection.

The following are *dwClaimType* types that are defined for the API:

| Claim Type | Description |
|------------|-------------|
| **NCRYPT_CLAIM_VBS_ROOT** | This type indicates that the generated claim is produced by the VBS root key. |
| **NCRYPT_CLAIM_VBS_IDENTITY** | This type indicates that the generated claim is produced by a VBS identity/attestation. This mean that the claim is produced by a VBS key that is elevated with the attestation flag **NCRYPT_ALLOW_KEY_ATTESTATION_FLAG** (see details below). |

The following are buffer types to be set in *pParameterList* buffer when verifying an attestation claim:

- **NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS**

  A new structure to be set as an **NCryptBuffer** item of type **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_ROOT_DETAILS** in **NCryptBufferDesc** output parameter of **NCryptVerifyClaim** with *dwClaimType* set to **NCRYPT_CLAIM_VBS_ROOT**. The structure definition is:

  ```cpp
  typedef struct _NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS
  {
      ULONG ulKeyFlags;
      ULONGLONG ullTrustletId;
      ULONG ulTrustletSecurityVersion;
      ULONG ulTrustletDebuggable;
  } NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS, *PNCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS;
  ```

  The structure includes these items:

  - **ulKeyFlags** – A combination of **NCRYPT_VBS_KEY_FLAG_\*** values that were set for the identity key.
  - **ullTrustletId** – A hard-coded identifier integer in the policy metadata of the VBS Trustlet that created the claim.
  - **ulTrustletSecurityVersion** – The Security Version number of the VBS Trustlet that created the claim. This version reflects which security updates have been applied to the trustlet and consequently implies the level of its security.
  - **ulTrustletDebuggable** – An indication if the VBS Trustlet that created the claim is debuggable. A `1` value indicates that the trustlet is debuggable and a `0` indicates of non-debuggable trustlet

  If further informative items are required in the future, then a new structure and a corresponding structure type will be defined.

  > [!NOTE]
  > This output parameter must be released after it’s no longer referenced.

- **NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS**

  A new structure to be set as an **NCryptBuffer** item of type **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_IDENTITY_DETAILS** in **NCryptBufferDesc** output parameter of **NCryptVerifyClaim** with *dwClaimType* set to **NCRYPT_CLAIM_VBS_IDENTITY**. The structure definition is:

  ```cpp
  typedef struct _NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS
  {
      ULONG ulKeyFlags;
      LPCWSTR pszSignatureHashAlg;
      ULONG ulPaddingScheme;
      LPCWSTR pszPaddingHashAlg;
      ULONG ulPaddingSalt;
  } NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS, *PNCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS;
  ```

  The structure includes these items:

  - **ulKeyFlags** – A combination of **NCRYPT_VBS_KEY_FLAG_\*** values that were set for the identity key.
  - **pszSignatureHashAlg** - A pointer to a Unicode string of the claim signature hash algorithm.
  - **ulPaddingScheme** - Padding scheme of the signing algorithm that was used through claim creation in [BCryptSignHash](/windows/win32/api/bcrypt/nf-bcrypt-bcryptsignhash).
  - **pszPaddingHashAlg** - A pointer to a Unicode string of the claim padding hash algorithm used through claim creation in [BCryptSignHash](/windows/win32/api/bcrypt/nf-bcrypt-bcryptsignhash).
  - **ulPaddingSalt** - Padding salt of the signing algorithm that was used through claim creation in [BCryptSignHash](/windows/win32/api/bcrypt/nf-bcrypt-bcryptsignhash).

  If further informative items are required in the future, then a new structure and a corresponding structure type will be defined.

  > [!NOTE]
  > This output parameter must be released after it’s no longer referenced. The sample code for releasing this parameter is given in the code example [below](#examples).

- **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_ROOT_DETAILS**

  A new buffer type to be set in a parameter **NCryptBuffer** in the **NCryptBufferDesc** *\*pOutput* parameter of **NCryptVerifyClaim**. This type indicates that the **NCryptBuffer** includes the data structure **NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS**.

- **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_IDENTITY_DETAILS**

  A new buffer type to be set in a parameter **NCryptBuffer** in the **NCryptBufferDesc** *\*pOutput* parameter of **NCryptVerifyClaim**. This type indicates that the **NCryptBuffer** includes the data structure **NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS**.

- **NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG**

  This is a new flag to be set in the **dwFlags** input parameter during verification of a VBS-generated claim. When this flag is set **NCryptVerifyClaim** produces the **NCryptBufferDesc** output parameter with an internal **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_ROOT_DETAILS** or **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_IDENTITY_DETAILS** parameter buffer type.

  The following table describes the relation between the input and output data structure types, in a successful scenario with **NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG**:

  | Input | Output |
  |-------|--------|
  | `dwClaimType = NCRYPT_CLAIM_VBS_ROOT` | **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_ROOT_DETAILS** buffer type with internal **NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS** informative structure. |
  | `dwClaimType = NCRYPT_CLAIM_VBS_IDENTITY` | **NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_IDENTITY_DETAILS** buffer type with internal **NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS** informative structure. |

#### Examples

This example illustrates the usage of the existing API to verify the attestation claims that were generated in with [NCryptCreateClaim](nf-ncrypt-ncryptcreateclaim.md).

The verification API may be invoked locally (on the machine that generated the claim blob) or remotely. The verification procedure requires these elements, corresponding to the claim generation keys:

- Claim blob
- Public attestation key blob
- Public token (general purpose) key blob

The verification API produces one of the output informative structures **NCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS** or **NCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS** if the input flag **NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG** is set. The memory of these structures is freed at the end of the code flow to avoid memory leaks.

```c
HRESULT VerifyClaim(
       BCRYPT_RSAKEY_BLOB *pAttestPublicKeyBlob,
       BCRYPT_RSAKEY_BLOB *pTokenPublicKeyBlob,
       PBYTE pRootClaim,
       DWORD rootClaimSize,
       PBYTE pIdentityClaim,
       DWORD identityClaimSize)
{

    HRESULT hr = S_OK;
    DWORD bytesWritten = 0;

    NCRYPT_PROV_HANDLE provider = NULL;

    if (FAILED(hr = NCryptOpenStorageProvider(&provider, MS_KEY_STORAGE_PROVIDER, 0)))
    {
        wprintf(L"Error opening storage provider in NCryptOpenStorageProvider: 0x%X\n", hr);
        goto cleanup;
    }

    NCRYPT_KEY_HANDLE attestPublicKey = NULL;

    if (FAILED(hr = NCryptImportKey(
                       provider,
                       NULL,
                       BCRYPT_RSAPUBLIC_BLOB,
                       NULL,
                       &attestPublicKey,
                       (PBYTE)pAttestPublicKeyBlob,
                       GetRsaPublicKeyBlobSize(pAttestPublicKeyBlob),
                       0)))
    {
        wprintf(L"Unable to create a key handle for attestation public key blob with NCryptImportKey(): 0x%X\n", hr);
        goto cleanup;
    }

    NCRYPT_KEY_HANDLE tokenPublicKey = NULL;

    if (FAILED(hr = NCryptImportKey(
                       provider,
                       NULL,
                       BCRYPT_RSAPUBLIC_BLOB,
                       NULL,
                       &tokenPublicKey,
                       (PBYTE)pTokenPublicKeyBlob,
                       GetRsaPublicKeyBlobSize(pTokenPublicKeyBlob),
                       0)))
    {
        wprintf(L"Unable to create a key handle for token public key blob with NCryptImportKey(): 0x%X\n", hr);
        goto cleanup;
    }

    NCryptBufferDesc rootOutput{};

    // Verify the VBS root claim using the attestation/identity public key
    if (FAILED(hr = NCryptVerifyClaim(
                       attestPublicKey,
                       NULL,
                       NCRYPT_CLAIM_VBS_ROOT, // Created claim by IDKS (VBS root signing key)
                       NULL, // parameters
                       pRootClaim,
                       rootClaimSize,
                       &rootOutput,
                       NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG /*dwFlags*/)))
    {
        switch (hr)
        {
            case STATUS_OBJECT_TYPE_MISMATCH:
                wprintf(L"The dwClaimType parameter’s value is different than the claim’s type.\n-----\n", hr);
                break;
            case STATUS_BAD_DATA:
                wprintf(L"Something wrong in one of the data structures. E.g. Magic value mismatch\n-----\n", hr);
                break;
            case STATUS_NO_MEMORY:
                wprintf(L"Memory allocation failed\n-----\n", hr);
                break;
            case STATUS_INVALID_PARAMETER:
                wprintf(L"Missing mandatory parameter or one of the parameters has a bad value.\n-----\n", hr);
                break;
            case STATUS_FAIL_CHECK:
                wprintf(L"One of the claim checks has failed.\n-----\n", hr);
                break;
            default:
                wprintf(L"Unable to verify VBS root claim from NCryptVerifyClaim(): 0x%X\n-----\n", hr);
        }
        goto cleanup;
    }

    PNCryptBuffer pRootOutBuffer;
    DWORD count;

    // Look into the retrieved VBS root claim details
    for (count = 0; count < rootOutput.cBuffers; ++count)
    {
        pRootOutBuffer = rootOutput.pBuffers[count];
        if (pRootOutBuffer->BufferType == NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_ROOT_DETAILS)
        {
            PNCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS pDetails =
            (PNCRYPT_VBS_ROOT_KEY_ATTESTATION_CLAIM_DETAILS) pRootOutBuffer->pvBuffer;
            wprintf(L"The claim trustlet id is: %lu\n-----\n", pDetails->ullTrustletId);
            wprintf(L"The claim trustlet Security Version number is: %llu\n-----\n", pDetails->ulTrustletSecurityVersion);
        }
    }

    NCryptBufferDesc identityOutput{};

    // Verify the identity claim using the attestation/identity and token public keys
    if (FAILED(hr = NCryptVerifyClaim(
                        tokenPublicKey,
                        attestPublicKey,
                        NCRYPT_CLAIM_VBS_IDENTITY, // Claim created by an attestation/identity key
                        NULL, // parameters
                        pIdentityClaim,
                        identityClaimSize,
                        &identityOutput,
                        NCRYPT_VBS_RETURN_CLAIM_DETAILS_FLAG /*dwFlags*/)))
    {
        wprintf(L"Unable to verify identity claim from NCryptVerifyClaim(): 0x%X\n-----\n", hr);
        goto cleanup;
    }

    PNCryptBuffer pIdentityOutBuffer;

    // Look into the retrieved identity claim details
    for (count = 0; count < identityOutput.cBuffers; ++count)
    {
        pIdentityOutBuffer = identityOutput.pBuffers[count];
        if (pIdentityOutBuffer->BufferType == NCRYPTBUFFER_VBS_ATTESTATION_STATEMENT_IDENTITY_DETAILS)
        {
            PNCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS pDetails =
            (PNCRYPT_VBS_IDENTITY_KEY_ATTESTATION_CLAIM_DETAILS) pIdentityOutBuffer->pvBuffer;
            wprintf(L"The claim hash algorithm is: %S\n-----\n", pDetails-> pszSignatureHashAlg);
            wprintf(L"The claim padding scheme is: %lu\n-----\n", pDetails->ulPaddingScheme);
        }
    }

    wprintf(L"Verify claim for root and identity types passed successfully\n");

    cleanup:

    if (provider != NULL)
    {
        NCryptFreeObject(provider);
    }
    if (attestPublicKey != NULL)
    {
        CryptDestroyKey(attestPublicKey);
    }
    if (tokenPub != NULL)
    {
        CryptDestroyKey(tokenPublicKey);
    }
    if (rootOutput.pBuffers != NULL)
    {
        for (count = 0; count < rootOutput.cBuffers; ++count)
        {
            NCryptFreeBuffer(rootOutput.pBuffers[count].pvBuffer);
        }
        NCryptFreeBuffer(rootOutput.pBuffers);
    }

    if (identityOutput.pBuffers != NULL)
    {
        for (count = 0; count < identityOutput.cBuffers; ++count)
        {
            NCryptFreeBuffer(identityOutput.pBuffers[count].pvBuffer);
        }
        NCryptFreeBuffer(identityOutput.pBuffers);
    }

    return hr;
}

DWORD GetRsaPublicKeyBlobSize(BCRYPT_RSAKEY_BLOB* publicKeyBlob)
{
    return sizeof(BCRYPT_RSAKEY_BLOB) +
                publicKeyBlob->cbModulus +
                publicKeyBlob->cbPublicExp;
}
```

## -returns

Returns a status code that indicates the success or failure of the function.

The following are some of the error codes that may be returned from the verification API when verifying VBS key protection attestation claims:

| Return Code | Meaning |
|-------------|---------|
| NTE_BAD_TYPE | The claim type input parameter is different from the type of the input claim blob. |
| STATUS_BAD_DATA | The input claim blob is invalid. |
| STATUS_NO_MEMORY | Memory (required for claim verification) allocation failed. |
| STATUS_INVALID_PARAMETER | Missing a mandatory input parameter or one of the parameters has an illegal value. |
| STATUS_FAIL_CHECK | The checks of the input blob claim have failed. |
| NTE_BAD_VER | The claim blob version doesn't match the verification implementation. |
| NTE_BAD_FLAGS | The flags provided in *dwFlags* are not supported. |
