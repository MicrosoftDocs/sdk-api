---
UID: NS:winnt._ENCLAVE_CREATE_INFO_SGX
title: ENCLAVE_CREATE_INFO_SGX (winnt.h)
description: Contains architecture-specific information to use to create an enclave when the enclave type is ENCLAVE_TYPE_SGX, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.
helpviewer_keywords: ["*PENCLAVE_CREATE_INFO_SGX","ENCLAVE_CREATE_INFO_SGX","ENCLAVE_CREATE_INFO_SGX structure","PENCLAVE_CREATE_INFO_SGX","PENCLAVE_CREATE_INFO_SGX structure pointer","base.enclave_create_info_sgx","winnt/ENCLAVE_CREATE_INFO_SGX","winnt/PENCLAVE_CREATE_INFO_SGX"]
old-location: base\enclave_create_info_sgx.htm
tech.root: base
ms.assetid: 51ED6E75-DA18-4CCE-8718-46328DD62B07
ms.date: 02/02/2024
ms.keywords: '*PENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX structure, PENCLAVE_CREATE_INFO_SGX, PENCLAVE_CREATE_INFO_SGX structure pointer, base.enclave_create_info_sgx, winnt/ENCLAVE_CREATE_INFO_SGX, winnt/PENCLAVE_CREATE_INFO_SGX'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: ENCLAVE_CREATE_INFO_SGX, *PENCLAVE_CREATE_INFO_SGX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCLAVE_CREATE_INFO_SGX
 - winnt/_ENCLAVE_CREATE_INFO_SGX
 - PENCLAVE_CREATE_INFO_SGX
 - winnt/PENCLAVE_CREATE_INFO_SGX
 - ENCLAVE_CREATE_INFO_SGX
 - winnt/ENCLAVE_CREATE_INFO_SGX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - ENCLAVE_CREATE_INFO_SGX
---

# ENCLAVE_CREATE_INFO_SGX structure

## -description

Contains architecture-specific information to use to create an enclave when the enclave type is **ENCLAVE_TYPE_SGX** or **ENCLAVE_TYPE_SGX2**, which specifies an enclave for one of the Intel Software Guard Extensions (SGX) architecture extensions.

## -struct-fields

### -field Secs

The SGX enclave control structure (**SECS**) to use to create the enclave.

## -remarks

For more information about the **SECS** structure, see the Intel SGX Programming Reference that is available from [Intel Software Guard Extensions](https://software.intel.com/sgx).

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[CreateEnclave](/windows/win32/api/enclaveapi/nf-enclaveapi-createenclave)

[ENCLAVE_INIT_INFO_SGX](/windows/win32/api/winnt/ns-winnt-enclave_init_info_sgx)
