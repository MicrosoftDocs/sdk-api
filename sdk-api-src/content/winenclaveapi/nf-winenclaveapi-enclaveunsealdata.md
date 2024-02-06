---
UID: NF:winenclaveapi.EnclaveUnsealData
title: EnclaveUnsealData function (winenclaveapi.h)
description: Decrypts an encrypted binary large object (blob).
helpviewer_keywords: ["ENCLAVE_UNSEAL_FLAG_STALE_KEY","EnclaveUnsealData","EnclaveUnsealData function","base.enclaveunsealdata","winenclaveapi/EnclaveUnsealData"]
old-location: base\enclaveunsealdata.htm
tech.root: base
ms.assetid: DDBDBEDE-E7EA-43B0-B2C7-B85D75EF3EB0
ms.date: 02/02/2024
ms.keywords: ENCLAVE_UNSEAL_FLAG_STALE_KEY, EnclaveUnsealData, EnclaveUnsealData function, base.enclaveunsealdata, winenclaveapi/EnclaveUnsealData
req.header: winenclaveapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vertdll.lib
req.dll: Vertdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnclaveUnsealData
 - winenclaveapi/EnclaveUnsealData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
api_name:
 - EnclaveUnsealData
---

# EnclaveUnsealData function

## -description

Decrypts an encrypted binary large object (blob).

## -parameters

### -param ProtectedBlob [in]

A pointer to the sealed data to unseal. This data may be stored either within the address range of the enclave or within the address space of the host process

### -param ProtectedBlobSize [in]

The size of the sealed data to unseal, in bytes.

### -param DecryptedData [out]

A pointer to a buffer where the unencrypted data should be placed. This data may be stored either within the address range of the enclave or within the address space of the host process. If this parameter is `NULL`, only the size of the decrypted data is calculated.

### -param BufferSize [in]

The size of the buffer to which the *DecryptedData* parameter points, in bytes. If *DecryptedData* is `NULL`, *BufferSize* must be zero. If *DecryptedData* is not `NULL`, and if the size of the decrypted data is larger than this value, an error is returned.

### -param DecryptedDataSize [out]

A pointer to a variable that receives the actual size of the decrypted data, in bytes.

### -param SealingIdentity [out, optional]

An optional pointer to a buffer that should be filled with the identity of the enclave that sealed the data. If this pointer is `NULL`, the  identity of the sealing enclave is not returned.

### -param UnsealingFlags [out, optional]

An optional pointer to a variable that receives zero or more of the following flags that describe the encrypted binary large object.

| Value | Meaning |
|-------|---------|
| **ENCLAVE_UNSEAL_FLAG_STALE_KEY**<br/>`1` | The data was encrypted with a stale key. Sealing keys are rotated when required for security, and the system can only maintain a fixed number of recently known keys. An enclave that determines that data was encrypted with a stale key should re-encrypt the data with a current key to minimize the chances that the key used to encrypt the data is no longer maintained in the key list. |

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

The enclave that calls **EnclaveUnsealData** must meet the criteria that correspond to the value of the [ENCLAVE_SEALING_IDENTITY_POLICY](../ntenclv/ne-ntenclv-enclave_sealing_identity_policy.md) that was specified by the enclave that sealed the data by calling [EnclaveSealData](nf-winenclaveapi-enclavesealdata.md).

**EnclaveUnsealData** must be called from within an enclave, and is only supported within enclaves that have the **ENCLAVE_TYPE_VBS** enclave type.

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[ENCLAVE_SEALING_IDENTITY_POLICY](../ntenclv/ne-ntenclv-enclave_sealing_identity_policy.md)

[EnclaveSealData](nf-winenclaveapi-enclavesealdata.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
