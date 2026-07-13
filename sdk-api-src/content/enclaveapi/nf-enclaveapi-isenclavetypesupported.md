---
UID: NF:enclaveapi.IsEnclaveTypeSupported
title: IsEnclaveTypeSupported function (enclaveapi.h)
description: Retrieves whether the specified type of enclave is supported.
helpviewer_keywords: ["ENCLAVE_TYPE_SGX", "ENCLAVE_TYPE_SGX2","ENCLAVE_TYPE_VBS","IsEnclaveTypeSupported","IsEnclaveTypeSupported function","base.isenclavetypesupported","base.isenclavetypesypported","enclaveapi/IsEnclaveTypeSupported"]
old-location: base\isenclavetypesupported.htm
tech.root: base
ms.assetid: E46AF02B-324F-43A8-8C73-9FE1E8E771E9
ms.date: 02/02/2024
ms.keywords: ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_SGX2, ENCLAVE_TYPE_VBS, IsEnclaveTypeSupported, IsEnclaveTypeSupported function, base.isenclavetypesupported, base.isenclavetypesypported, enclaveapi/IsEnclaveTypeSupported
req.header: enclaveapi.h
req.include-header: Winbase.h
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
req.lib: Kernel32.lib
req.dll: Api-ms-win-core-enclave-l1-1-0.dll; Kernel32.dll; KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsEnclaveTypeSupported
 - enclaveapi/IsEnclaveTypeSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-enclave-l1-1-1.dll
 - api-ms-win-core-enclave-l1-1-0.dll
 - kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-Enclave-L1-1-0.dll
api_name:
 - IsEnclaveTypeSupported
---

# IsEnclaveTypeSupported function

## -description

Retrieves whether the specified type of enclave is supported.

## -parameters

### -param flEnclaveType [in]

The type of enclave to check.

| Value | Meaning |
| --- | --- |
| **ENCLAVE_TYPE_SGX**<br/>`0x00000001` | An enclave for the Intel Software Guard Extensions (SGX) architecture extension. |
| **ENCLAVE_TYPE_SGX2**<br/>`0x00000002` | Supports SGX2 and SGX1 enclaves. The platform and OS support SGX2 instructions with EDMM on this platform (in addition to other SGX2 constructs). |
| **ENCLAVE_TYPE_VBS**<br/>`0x00000010` | A virtualization-based security (VBS) enclave. |

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

For a list of common error codes, see [System Error Codes](/windows/desktop/Debug/system-error-codes). The following error codes also apply for this function.

| Return code | Description |
| --- | --- |
| **ERROR_NOT_SUPPORTED** | An unsupported enclave type was specified. |

## -remarks

**ENCLAVE_TYPE_SGX2** will change some things about how the OS handles SGX functionality:

- It will support the new extensions to **VirtualAlloc**, **VirtualFree**, and **VirtualProtect**.

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)
