---
UID: NF:ncrypt.NCryptImportKey
title: NCryptImportKey function (ncrypt.h)
description: Imports a Cryptography API - Next Generation (CNG) key from a memory BLOB.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptImportKey","NCryptImportKey function [Security]","ncrypt/NCryptImportKey","security.ncryptimportkey_func"]
old-location: security\ncryptimportkey_func.htm
tech.root: security
ms.assetid: ede0e7e0-cb2c-44c0-b724-58db3480b781
ms.date: 06/25/2025
ms.keywords: NCRYPT_SILENT_FLAG, NCryptImportKey, NCryptImportKey function [Security], ncrypt/NCryptImportKey, security.ncryptimportkey_func
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptImportKey
 - ncrypt/NCryptImportKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptImportKey
---

# NCryptImportKey function

## -description

The **NCryptImportKey** function imports a Cryptography API: Next Generation (CNG) key from a memory [BLOB](/windows/win32/SecGloss/b-gly).

## -parameters

### -param hProvider [in]

The handle of the key storage provider.

### -param hImportKey [in, optional]

The handle of the [cryptographic key](/windows/win32/SecGloss/c-gly) with which the key data within the imported [key BLOB](/windows/win32/SecGloss/k-gly) was encrypted. This must be a handle to the same key that was passed in the _hExportKey_ parameter of the [NCryptExportKey](/windows/win32/api/ncrypt/nf-ncrypt-ncryptexportkey) function. If this parameter is **NULL**, the key BLOB is assumed to not be encrypted.

### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the format of the key BLOB. These formats are specific to a particular key storage provider. For the BLOB formats supported by Microsoft providers, see [Remarks](#-remarks).

### -param pParameterList [in, optional]

The address of an [NCryptBufferDesc](/windows/win32/api/bcrypt/ns-bcrypt-bcryptbufferdesc) structure that points to an array of buffers that contain parameter information for the key.

### -param phKey [out]

The address of an **NCRYPT_KEY_HANDLE** variable that receives the handle of the key. When you have finished using this handle, release it by passing it to the [NCryptFreeObject](/windows/win32/api/ncrypt/nf-ncrypt-ncryptfreeobject) function.

### -param pbData [in]

The address of a buffer that contains the key BLOB to be imported. The _cbData_ parameter contains the size of this buffer.

### -param cbData [in]

The size, in bytes, of the _pbData_ buffer.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values. The set of valid flags is specific to each key storage provider.

| Value | Meaning |
|--------|--------|
| **NCRYPT_SILENT_FLAG** | Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the **NTE_SILENT_CONTEXT** error code as the last error. |
| **NCRYPT_REQUIRE_VBS_FLAG** | Indicates a key must be protected with Virtualization-based security (VBS). By default, this creates a cross-boot persisted key stored on disk that persists across reboot cycles.<br/><br/>Operation will fail if VBS is not available. (**\*See Remarks**) |
| **NCRYPT_PREFER_VBS_FLAG** | Indicates a key should be protected with Virtualization-based security (VBS). By default, this creates a cross-boot persisted key stored on disk that persists across reboot cycles.<br/><br/>Operation will generate a software-isolated key if VBS is not available. (**\*See Remarks**) |
| **NCRYPT_USE_PER_BOOT_KEY_FLAG** | An additional flag that can be used along with **NCRYPT_REQUIRE_VBS_FLAG** or **NCRYPT_PREFER_VBS_FLAG**. Instructs Virtualization-based security (VBS) to protect the client key with a per-boot key that is stored in disk but can't be reused across boot cycles. (**\*See Remarks**) |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|--------|--------|
| **ERROR_SUCCESS** | The function was successful. |
| **NTE_BAD_FLAGS** | The _dwFlags_ parameter contains a value that is not valid. |
| **NTE_EXISTS** | A key with the specified name already exists and the **NCRYPT_OVERWRITE_KEY_FLAG** was not specified. |
| **NTE_INVALID_HANDLE** | The _hProvider_ parameter is not valid. |
| **NTE_INVALID_PARAMETER** | One or more parameters are not valid. |
| **NTE_NO_MEMORY** | A memory allocation failure occurred. |
| **NTE_VBS_UNAVAILABLE** | VBS is unavailable. |
| **NTE_VBS_CANNOT_DECRYPT_KEY** | VBS failed decryption operation. |

## -remarks

> [!IMPORTANT]
> Information regarding VBS flags relates to prerelease product that may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

A service must not call this function from its [StartService Function](/windows/win32/api/winsvc/nf-winsvc-startservicea). If a service calls this function from its **StartService** function, a deadlock can occur, and the service may stop responding.

The following sections describe behaviors specific to the Microsoft key storage providers:

- **Microsoft Software KSP**
- **Microsoft Smart Card KSP**

#### Microsoft Software KSP

Refer to [NCryptImportKey](nf-ncrypt-ncryptimportkey.md) for details of most *pszBlobType* parameters supported by the Microsoft software KSP.

If a key name is not supplied, the Microsoft Software KSP treats the key as ephemeral and does not store it persistently. For the **NCRYPT_OPAQUETRANSPORT_BLOB** type, the key name is stored within the BLOB when it is exported. For other BLOB formats, the name can be supplied in an **NCRYPTBUFFER_PKCS_KEY_NAME** buffer parameter within the _pParameterList_ parameter.

On Windows Server 2008 and Windows Vista, only keys imported as PKCS #7 envelope BLOBs (**NCRYPT_PKCS7_ENVELOPE_BLOB**) or PKCS #8 private key BLOBs (**NCRYPT_PKCS8_PRIVATE_KEY_BLOB**) can be persisted by using the above method. To persist keys imported through other BLOB types on these platforms, use the method documented in [Key Import and Export](/windows/win32/SecCNG/key-import-and-export).

The following flags are supported by this KSP.

| Term | Description |
|--------|--------|
| NCRYPT_NO_KEY_VALIDATION | Do not validate the public portion of the key pair. This flag only applies to public/private key pairs. |
| NCRYPT_DO_NOT_FINALIZE_FLAG | Do not finalize the key. This option is useful when you need to add or modify properties of the key after importing it. You must finalize the key before it can be used by passing the key handle to the [NCryptFinalizeKey](/windows/win32/api/ncrypt/nf-ncrypt-ncryptfinalizekey) function. This flag is supported for the private keys PKCS #7 and PKCS #8 but not public keys. |
| NCRYPT_MACHINE_KEY_FLAG | The key applies to the local computer. If this flag is not present, the key applies to the current user. |
| NCRYPT_OVERWRITE_KEY_FLAG | If a key already exists in the container with the specified name, the existing key will be overwritten. If this flag is not specified and a key with the specified name already exists, this function will return **NTE_EXISTS**. |
| NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG | Also save the key in legacy storage. This allows the key to be used with the CryptoAPI. This flag only applies to RSA keys. |

#### Microsoft Smart Card KSP

The set of key BLOB formats and flags supported by this KSP is identical to the set supported by the Microsoft Software KSP.

On Windows Server 2008 and Windows Vista, the Microsoft Smart Card KSP imports all keys into the Microsoft Software KSP. Thus, keys cannot be persisted on to a smart card by using this API, and the guidance in the above section applies when trying to persist keys within the Microsoft Software KSP.

On Windows Server 2008 R2 and Windows 7, the Microsoft Smart Card Key Storage Provider can import a private key to a smart card, provided the following conditions are met:

- The key container name on the card is valid.
- Importing private keys is supported by the smart card.
- The following two registry keys are set to a **DWORD** of `0x1`:
  - **HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider\\Microsoft Base Smart Card Crypto Provider\\AllowPrivateExchangeKeyImport**
  - **HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider\\Microsoft Base Smart Card Crypto Provider\\AllowPrivateSignatureKeyImport**

If the key container name is **NULL**, the Microsoft Smart Card KSP treats the key as ephemeral and imports it into the Microsoft Software KSP.

#### Additional hardware requirements for VBS keys

Although you may have the appropriate OS installed on your machine, the following additional hardware requirements must be met to use VBS to generate and protect keys.

- VBS enabled (see [Virtualization-based security (VBS)](/windows-hardware/design/device-experiences/oem-vbs))
- TPM enabled
  - For bare-metal environments, TPM 2.0 is required.
  - For VM environments, vTPM (Virtual TPM) is supported.
- BIOS should be upgraded to UEFI with SecureBoot profile

For more information about hardware requirements:

- VBS has several hardware requirements to run, including Hyper-V (Windows hypervisor), 64 bit architecture, and IOMMU support. The full list of VBS hardware requirements can be found [here](/windows-hardware/design/device-experiences/oem-vbs).
- Requirements for a highly secure device can be found [here](/windows-hardware/design/device-experiences/oem-highly-secure).

## -see-also

[NCryptBuffer](../bcrypt/ns-bcrypt-bcryptbuffer.md)

[NCryptCreatePersistedKey](nf-ncrypt-ncryptcreatepersistedkey.md)
