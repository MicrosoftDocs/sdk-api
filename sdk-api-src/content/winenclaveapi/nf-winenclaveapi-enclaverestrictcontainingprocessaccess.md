---
UID: NF:winenclaveapi.EnclaveRestrictContainingProcessAccess
tech.root: base
title: EnclaveRestrictContainingProcessAccess function (winenclaveapi.h)
ms.date: 04/11/2025
targetos: Windows
description: This function restricts (or restores) access by an enclave to the address space of its containing process.
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
 - EnclaveRestrictContainingProcessAccess
f1_keywords:
 - EnclaveRestrictContainingProcessAccess
 - winenclaveapi/EnclaveRestrictContainingProcessAccess
dev_langs:
 - c++
helpviewer_keywords:
 - EnclaveRestrictContainingProcessAccess
---

## -description

Restricts (or restores) access by an enclave to the address space of its containing process. This policy applies to all threads in the enclave.

## -parameters

### -param RestrictAccess

Set this value to `TRUE` if the process should restrict (i.e. disable) access to the address space of the containing process. Otherwise, set it to `FALSE` if restrictions should be relaxed, and the containing address space should be accessible.

### -param PreviouslyRestricted

A pointer to a variable that will receive the previous state of the restriction.

## -returns

An `HRESULT` value that indicates the success or failure of the operation.

## -remarks

When access is restricted, attempting to access the address space of the containing process from the enclave will result in an access violation. However, even when access is restricted, the [EnclaveCopyOutOfEnclave](nf-winenclaveapi-enclavecopyoutofenclave.md) and [EnclaveCopyIntoEnclave](nf-winenclaveapi-enclavecopyintoenclave.md) APIs continue to permit access to the address space of the containing process.

Access to the containing process's address space can also be restricted by setting the [IMAGE_ENCLAVE_POLICY_STRICT_MEMORY](../winnt/ns-winnt-image_enclave_config64.md#-field-enclaveflags) flag in the enclave's image configuration. The **EnclaveRestrictContainingProcessAccess** API can be used to change this policy at runtime.

## -see-also

[EnclaveCopyOutOfEnclave](nf-winenclaveapi-enclavecopyoutofenclave.md)

[EnclaveCopyIntoEnclave](nf-winenclaveapi-enclavecopyintoenclave.md)
