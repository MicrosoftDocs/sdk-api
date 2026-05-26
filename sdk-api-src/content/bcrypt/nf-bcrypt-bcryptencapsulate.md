---
UID: NF:bcrypt.BCryptEncapsulate
title: BCryptEncapsulate function (bcrypt.h)
description: Uses a key encapsulation mechanism (KEM) to generate a shared secret key and encrypt it to produce a KEM ciphertext.
helpviewer_keywords: ["BCryptEncapsulate","BCryptEncapsulate function [Security]","bcrypt/BCryptEncapsulate","security.bcryptencapsulate", "BCrypt KEM"]
old-location: security\bcryptencapsulate.htm
tech.root: security
ms.assetid:
ms.date: 5/22/2025
ms.keywords: BCryptEncapsulate, BCryptEncapsulate function [Security], bcrypt/BCryptEncapsulate, security.bcryptencapsulate, BCrypt KEM
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 24H2
f1_keywords:
 - BCryptEncapsulate
 - bcrypt/BCryptEncapsulate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptEncapsulate
original_content_git_url: https://github.com/MicrosoftDocs/win32-pr/blob/live/desktop-src/SecCNG/bcrypt/nf-bcrypt-bcryptencapsulate.md
---

# BCryptEncapsulate function - Win32 apps | Microsoft Learn

Note

Some information relates to a prerelease product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here. The feature described in this topic is available in pre-release versions of the [Windows Insider Preview](https://www.microsoft.com/software-download/windowsinsiderpreviewSDK).

The **BCryptEncapsulate** function performs the Encapsulation operation of a Key Encapsulation Mechanism (KEM). It generates a shared secret key and encrypts it with the provided public key to produce a KEM ciphertext, returning both the shared secret key and the KEM ciphertext.

## Syntax

```cpp
NTSTATUS BCryptEncapsulate(
  _In_  BCRYPT_KEY_HANDLE hKey,
  _Out_writes_bytes_to_opt_(cbSecretKey ,*pcbSecretKey)
        PUCHAR            pbSecretKey,
  _In_  ULONG             cbSecretKey,
  _Out_ ULONG             *pcbSecretKey,
  _Out_writes_bytes_to_opt_(cbCipherText ,*pcbCipherText)
        PUCHAR            pbCipherText,
  _In_  ULONG             cbCipherText,
  _Out_ ULONG             *pcbCipherText,
  _In_  ULONG             dwFlags
);
```

## Parameters

*hKey*`[in]`

The handle of the key to use for the encapsulation operation. This key must contain a public (encapsulation) key, and the handle would typically be obtained by using [BCryptImportKeyPair](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) with a [public key](/en-us/windows/desktop/SecGloss/p-gly) BLOB for the KEM algorithm. It is also possible to use a private key handle for the encapsulation operation, as KEM private key handles represent a key pair.

*pbSecretKey*`[out]`

A pointer to a buffer that receives the shared secret key. See remarks for more information.

*cbSecretKey*`[in]`

The size, in bytes, of the *pbSecretKey* buffer.

*pcbSecretKey*`[out]`

A pointer to a **ULONG** variable that the receives the number of bytes written to *pbSecretKey* buffer.

If *pbSecretKey* is `NULL`, this receives the size, in bytes, required for the shared secret key. See remarks for more information.

*pbCipherText*`[out]`

A pointer to a buffer that receives the KEM ciphertext. See remarks for more information.

*cbCipherText*`[in]`

The size, in bytes, of the *pbCipherText* buffer.

*pcbCipherText*`[out]`

A pointer to a **ULONG** variable that the receives the number of bytes written to *pbCipherText* buffer.

If *pbCipherText* is `NULL`, this receives the size, in bytes, required for the KEM ciphertext. See remarks for more information.

*dwFlags*`[in]`

Reserved, must be zero.

## Return value

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following.

| Return Code | Description |
| --- | --- |
| `STATUS_SUCCESS` | The function was successful. |
| `STATUS_INVALID_PARAMETER` | One or more required parameters (*hKey*, *pcbSecretKey*, *pcbCipherText*) is `NULL`, or one of the parameters has an invalid value. |
| `STATUS_INVALID_BUFFER_SIZE` | A buffer size (*cbSecretKey*, *cbCipherText*) does not match the expected size for the KEM parameters associated with the encapsulation key. \*pcbSecretKey receives the number of bytes required for *pbSecretKey*, *pcbCipherText* receives the number of bytes required for *pbCipherText*. |
| `STATUS_BUFFER_TOO_SMALL` | An output buffer size (*cbSecretKey*, *cbCipherText*) is too small for the result encapsulation operation for the KEM parameters associated with the encapsulation key. *pcbSecretKey* receives the number of bytes required for *pbSecretKey*, *pcbCipherText* receives the number of bytes required for *pbCipherText*. |

## Remarks

To query the required sizes of the *pbSecretKey* and *pbCipherText* buffers, callers may call **BCryptEncapsulate** with `NULL`*pbSecretKey* and *pbCipherText*. The required sizes will be returned in *pcbSecretKey* and *pcbCipherText*, respectively. This query is efficient and returns the size without performing the encapsulation. Equivalently, use [BCryptGetProperty](/en-us/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) to query the **BCRYPT\_KEM\_SHARED\_SECRET\_LENGTH** property of the algorithm or key handle, and the **BCRYPT\_KEM\_CIPHERTEXT\_LENGTH** property of the key handle. For currently supported KEM algorithms (ML-KEM), the shared secret length is a constant size for a given algorithm and the KEM ciphertext length is a constant size for a given parameter set.

## Requirements

| Requirement | Value |
| --- | --- |
| **Minimum supported client** | **Windows 11 24H2:** Support for ML-KEM begins. [desktop apps only] |
| **Minimum supported server** | **Windows Server 2025:** Support for ML-KEM begins. [desktop apps only] |
| **Library** | `Bcrypt.lib` |
| **DLL** | `Bcrypt.dll` |
