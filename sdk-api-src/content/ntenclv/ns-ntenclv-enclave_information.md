---
UID: NS:ntenclv.ENCLAVE_INFORMATION
title: ENCLAVE_INFORMATION (ntenclv.h)
description: Contains information about the currently executing enclave.
helpviewer_keywords: ["ENCLAVE_INFORMATION","ENCLAVE_INFORMATION structure","ENCLAVE_TYPE_SGX","ENCLAVE_TYPE_VBS","base.enclave_information","ntenclv/ENCLAVE_INFORMATION"]
old-location: base\enclave_information.htm
tech.root: base
ms.assetid: 6720EDBE-6A0E-4192-A096-2ACA681E2AAF
ms.date: 02/02/2024
ms.keywords: ENCLAVE_INFORMATION, ENCLAVE_INFORMATION structure, ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, base.enclave_information, ntenclv/ENCLAVE_INFORMATION
req.header: ntenclv.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENCLAVE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ENCLAVE_INFORMATION
 - ntenclv/ENCLAVE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntenclv.h
api_name:
 - ENCLAVE_INFORMATION
---

# ENCLAVE_INFORMATION structure

## -description

Contains information about the currently executing enclave.

## -struct-fields

### -field EnclaveType

The architecture type of the enclave.

| Value | Meaning |
|-------|---------|
| **ENCLAVE_TYPE_SGX**<br/>`0x00000001` | An enclave for the Intel Software Guard Extensions (SGX) architecture extension. |
| **ENCLAVE_TYPE_SGX2**<br/>`0x00000002` | Supports SGX2 and SGX1 enclaves. The platform and OS support SGX2 instructions with EDMM on this platform (in addition to other SGX2 constructs). |
| **ENCLAVE_TYPE_VBS**<br/>`0x00000010` | A VBS enclave. |

### -field Reserved

Reserved.

### -field BaseAddress

A pointer to the base address of the enclave.

### -field Size

The size of the enclave, in bytes.

### -field Identity

The identity of the primary module of an enclave.

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[ENCLAVE_IDENTITY](ns-ntenclv-enclave_identity.md)

[EnclaveGetEnclaveInformation](../winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation.md)
