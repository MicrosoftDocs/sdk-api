---
UID: NS:bcrypt._BCRYPT_PQDSA_KEY_BLOB
title: BCRYPT_PQDSA_KEY_BLOB (bcrypt.h)
description: Structure used for post-quantum digital signature algorithm key BLOBs.
helpviewer_keywords: ["BCRYPT_PQDSA_KEY_BLOB","BCRYPT_PQDSA_KEY_BLOB structure [Security]","bcrypt/BCRYPT_PQDSA_KEY_BLOB","security.bcrypt_pqdsa_key_blob"]
old-location: 
tech.root: security
ms.assetid: 
ms.date: 05/26/2026
ms.keywords: BCRYPT_PQDSA_KEY_BLOB, BCRYPT_PQDSA_KEY_BLOB structure [Security], bcrypt/BCRYPT_PQDSA_KEY_BLOB, security.bcrypt_pqdsa_key_blob
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 24H2
req.target-min-winversvr: Windows Server 2025
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
req.typenames: BCRYPT_PQDSA_KEY_BLOB
req.redist: 
ms.custom: 24H2
f1_keywords:
 - _BCRYPT_PQDSA_KEY_BLOB
 - bcrypt/_BCRYPT_PQDSA_KEY_BLOB
 - BCRYPT_PQDSA_KEY_BLOB
 - bcrypt/BCRYPT_PQDSA_KEY_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_PQDSA_KEY_BLOB
---

# BCRYPT_PQDSA_KEY_BLOB structure - Win32 apps | Microsoft Learn

Note

Some information relates to a prerelease product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here. The feature described in this topic is available in pre-release versions of the [Windows Insider Preview](https://www.microsoft.com/software-download/windowsinsiderpreviewSDK).

This structure is used to import and export keys for Post-Quantum Digital Signature algorithms (PQDSA). The **BCRYPT\_PQDSA\_KEY\_BLOB** structure is used as a header for a Post-Quantum Digital Signature algorithm (PQDSA) [public key](/en-us/windows/win32/SecGloss/p-gly) (byte-encoded encapsulation key) or [private key](/en-us/windows/win32/SecGloss/p-gly) [BLOB](/en-us/windows/win32/SecGloss/b-gly) in memory.

## Syntax

```cpp
typedef struct _BCRYPT_PQDSA_KEY_BLOB {
  ULONG dwMagic;
  ULONG cbParameterSet;                                   // Byte size of parameterSet[]
  ULONG cbKey;                                            // Byte size of key[]
  // WCHAR parameterSet[cbParameterSet / sizeof(WCHAR)];  // Including \0 terminator
  // BYTE key[cbKey];                                     // Key material
} BCRYPT_PQDSA_KEY_BLOB, *PBCRYPT_PQDSA_KEY_BLOB;
```

## Fields

### dwMagic

The **dwMagic** field is a 4-byte value that indicates the format of the key being used. The following values are defined:

| Value | Meaning |
| --- | --- |
| **BCRYPT\_MLDSA\_PUBLIC\_MAGIC**`0x4B505344` | The structure represents a public key. |
| **BCRYPT\_MLDSA\_PRIVATE\_MAGIC**`0x4B535344` | The structure represents an expanded private key. |
| **BCRYPT\_MLDSA\_PRIVATE\_SEED\_MAGIC**`0x53535344` | The structure represents a private seed. |

### cbParameterSet

The length, in bytes, of the buffer `parameterSet` directly following the struct. This buffer contains a null-terminated Unicode string that identifies the parameter set of the key. The following values are currently supported:

| parameterSet | cbParameterSet | Meaning |
| --- | --- | --- |
| **BCRYPT\_MLDSA\_PARAMETER\_SET\_44**`L"44"` | 6 | ML-DSA-44, security category 2. |
| **BCRYPT\_MLDSA\_PARAMETER\_SET\_65**`L"65"` | 6 | ML-DSA-65, security category 3. |
| **BCRYPT\_MLDSA\_PARAMETER\_SET\_87**`L"87"` | 6 | ML-DSA-87, security category 5. |

### cbKey

The length, in bytes, of the buffer **key** directly following **parameterSet**. This size is static and depends on the key format and parameter set in use.

## Remarks

The consumers of Post-Quantum Digital Signature algorithms will use the same subset of the BCrypt API as the existing (non-Post-Quantum) Digital Signature Algorithms supported by CNG in order to perform the operations the algorithms support. These are:

- Algorithm handle manipulation: [BCryptOpenAlgorithmProvider](/en-us/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider), [BCryptCloseAlgorithmProvider](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider)
- Key management: [BCryptGenerateKeyPair](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair), [BCryptImportKeyPair](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair), [BCryptExportKey](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey), [BCryptDestroyKey](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroykey), [BCryptFinalizeKeyPair](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinalizekeypair)
- Signature generation/verification: [BCryptSignHash](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash), [BCryptVerifySignature](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature)
- Updating/Querying properties: [BCryptGetProperty](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty), [BCryptSetProperty](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty)

## Requirements

| Requirement | Value |
| --- | --- |
| **Minimum supported client** | **Windows 11 24H2:** Support for ML-DSA begins. [desktop apps only] |
| **Minimum supported server** | **Windows Server 2025:** Support for ML-DSA begins. [desktop apps only] |
| **Header** | `bcrypt.h` |