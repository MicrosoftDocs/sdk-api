---
UID: NF:ncrypt.NCryptCreatePersistedKey
title: NCryptCreatePersistedKey function (ncrypt.h)
description: Creates a new key and stores it in the specified key storage provider.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","NCRYPT_MACHINE_KEY_FLAG","NCRYPT_OVERWRITE_KEY_FLAG","NCryptCreatePersistedKey","NCryptCreatePersistedKey function [Security]","ncrypt/NCryptCreatePersistedKey","security.ncryptcreatepersistedkey_func"]
old-location: security\ncryptcreatepersistedkey_func.htm
tech.root: security
ms.assetid: eeb1842f-fd9e-4edf-9db8-7b4e91760e9b
ms.date: 05/29/2024
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, NCRYPT_MACHINE_KEY_FLAG, NCRYPT_OVERWRITE_KEY_FLAG, NCryptCreatePersistedKey, NCryptCreatePersistedKey function [Security], ncrypt/NCryptCreatePersistedKey, security.ncryptcreatepersistedkey_func
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
 - NCryptCreatePersistedKey
 - ncrypt/NCryptCreatePersistedKey
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
 - NCryptCreatePersistedKey
---

# NCryptCreatePersistedKey function

## -description

The **NCryptCreatePersistedKey** function creates a new key and stores it in the specified key storage provider. After you create a key by using this function, you can use the [NCryptSetProperty](nf-ncrypt-ncryptsetproperty.md) function to set its properties; however, the key cannot be used until the [NCryptFinalizeKey](nf-ncrypt-ncryptfinalizekey.md) function is called.

## -parameters

### -param hProvider [in]

The handle of the key storage provider to create the key in. This handle is obtained by using the [NCryptOpenStorageProvider](nf-ncrypt-ncryptopenstorageprovider.md) function.

### -param phKey [out]

The address of an **NCRYPT_KEY_HANDLE** variable that receives the handle of the key. When you have finished using this handle, release it by passing it to the [NCryptFreeObject](nf-ncrypt-ncryptfreeobject.md) function. To delete the key file on disk, pass the handle to the [NCryptDeleteKey](nf-ncrypt-ncryptdeletekey.md) function. This will also release the handle. So applications may pass the handle to either **NCryptFreeObject** or **NCryptDeleteKey**, but not both.

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic algorithm to create the key. This can be one of the standard [CNG Algorithm Identifiers](/windows/win32/SecCNG/cng-algorithm-identifiers) or the identifier for another registered algorithm.

### -param pszKeyName [in, optional]

A pointer to a null-terminated Unicode string that contains the name of the key. If this parameter is **NULL**, this function will create an ephemeral key that is not persisted.

### -param dwLegacyKeySpec [in]

A legacy identifier that specifies the type of key. This can be one of the following values:

| Value | Meaning |
| ----- | ------- |
| **AT_KEYEXCHANGE** | The key is a key exchange key. |
| **AT_SIGNATURE** | The key is a signature key. |
| 0 | The key is none of the above types. |

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or a combination of one or more of the following values:

| Value | Meaning |
| ----- | ------- |
| **NCRYPT_MACHINE_KEY_FLAG** | The key applies to the local computer. If this flag is not present, the key applies to the current user. |
| **NCRYPT_OVERWRITE_KEY_FLAG** | If a key already exists in the container with the specified name, the existing key will be overwritten. If this flag is not specified and a key with the specified name already exists, this function will return **NTE_EXISTS**. |
| **NCRYPT_REQUIRE_VBS_FLAG** | Indicates a key must be protected with Virtualization-based security (VBS). By default, this creates a cross-boot persisted key stored on disk that persists across reboot cycles. <br/><br/>Operation will fail if VBS is not available. (**\*See Remarks**) |
| **NCRYPT_PREFER_VBS_FLAG** | Indicates a key should be protected with Virtualization-based security (VBS). By default, this creates a cross-boot persisted key stored on disk that persists across reboot cycles <br/><br/>Operation will generate a software-isolated key if VBS is not available. (**\*See Remarks**) |
| **NCRYPT_USE_PER_BOOT_KEY_FLAG** | An additional flag that can be used along with **NCRYPT_REQUIRE_VBS_FLAG** or **NCRYPT_PREFER_VBS_FLAG**. Instructs Virtualization-based security (VBS) to protect the client key with a per-boot key that is stored in disk but can't be reused across boot cycles. (**\*See Remarks**) |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
| ----------- | ----------- |
| **ERROR_SUCCESS** | The function was successful. |
| **NTE_BAD_FLAGS** | The *dwFlags* parameter contains a value that is not valid. |
| **NTE_EXISTS** | A key with the specified name already exists and the **NCRYPT_OVERWRITE_KEY_FLAG** was not specified. |
| **NTE_INVALID_HANDLE** | The *hProvider* parameter is not valid. |
| **NTE_INVALID_PARAMETER** | One or more parameters are not valid. |
| **NTE_NO_MEMORY** | A memory allocation failure occurred. |
| **NTE_VBS_UNAVAILABLE** | VBS is unavailable. |

## -remarks

> [!IMPORTANT]
> Information regarding VBS flags relates to prerelease product that may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

If you are creating an RSA key pair, you can also have the key stored in legacy storage so that it can be used with the CryptoAPI by passing the **NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG** flag to the [NCryptFinalizeKey](nf-ncrypt-ncryptfinalizekey.md) function when the key is finalized.

A service must not call this function from its [StartService Function](/windows/win32/api/winsvc/nf-winsvc-startservicea). If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

### Additional hardware requirements for VBS keys

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

[NCryptDeleteKey](nf-ncrypt-ncryptdeletekey.md)

[NCryptFinalizeKey](nf-ncrypt-ncryptfinalizekey.md)

[NCryptImportKey](nf-ncrypt-ncryptimportkey.md)
