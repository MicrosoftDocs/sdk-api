---
UID: NF:winenclaveapi.EnclaveCopyIntoEnclave
tech.root: base
title: EnclaveCopyIntoEnclave function (winenclaveapi.h)
ms.date: 04/11/2025
targetos: Windows
description: Copies data from an unsecure address (outside of the enclave) into the enclave.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Vertdll.dll
req.header: winenclaveapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Vertdll.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 24H2 [desktop apps only]
req.target-min-winversvr: Windows Server 2025 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winenclaveapi.h
api_name:
 - EnclaveCopyIntoEnclave
f1_keywords:
 - EnclaveCopyIntoEnclave
 - winenclaveapi/EnclaveCopyIntoEnclave
dev_langs:
 - c++
helpviewer_keywords:
 - EnclaveCopyIntoEnclave
---

## -description

Copies data from an untrusted address (outside of the enclave) into the enclave.

## -parameters

### -param EnclaveAddress

An address within the enclave to which to copy data.

### -param UnsecureAddress

An address outside of the enclave from which to copy data.

### -param NumberOfBytes

The number of bytes to copy.

## -returns

An HRESULT value that indicates success or failure. The function returns `S_OK` if the copy operation was successful. Otherwise, it returns an HRESULT error code.

## -remarks

Note that the [EnclaveCopyOutOfEnclave](nf-winenclaveapi-enclavecopyoutofenclave.md) and **EnclaveCopyIntoEnclave** APIs will still continue to work (and access the address space of the containing process) even when access is restricted using [EnclaveRestrictContainingProcessAccess](nf-winenclaveapi-enclaverestrictcontainingprocessaccess.md).

## -see-also

[EnclaveCopyOutOfEnclave](nf-winenclaveapi-enclavecopyoutofenclave.md)

[EnclaveRestrictContainingProcessAccess](nf-winenclaveapi-enclaverestrictcontainingprocessaccess.md)
