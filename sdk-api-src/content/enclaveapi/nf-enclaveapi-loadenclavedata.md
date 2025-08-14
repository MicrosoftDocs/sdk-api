---
UID: NF:enclaveapi.LoadEnclaveData
title: LoadEnclaveData function (enclaveapi.h)
description: Loads data into an uninitialized enclave that you created by calling CreateEnclave.
helpviewer_keywords: ["LoadEnclaveData","LoadEnclaveData function","base.loadenclavedata","enclaveapi/LoadEnclaveData"]
old-location: base\loadenclavedata.htm
tech.root: base
ms.assetid: CC696026-FB74-4D91-BB40-17610DF41F8F
ms.date: 02/02/2024
ms.keywords: LoadEnclaveData, LoadEnclaveData function, base.loadenclavedata, enclaveapi/LoadEnclaveData
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
req.lib: onecore.lib
req.dll: Api-ms-win-core-enclave-l1-1-0.dll; kernel32.dll; KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadEnclaveData
 - enclaveapi/LoadEnclaveData
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
 - LoadEnclaveData
---

# LoadEnclaveData function

## -description

Loads data into an  uninitialized enclave that you created by calling [CreateEnclave](nf-enclaveapi-createenclave.md).

## -parameters

### -param hProcess [in]

A handle to the process for which the enclave was created.

### -param lpAddress [in]

The address in the enclave where you want to load the data.

### -param lpBuffer [in]

A pointer to the data the you want to load into the enclave.

### -param nSize [in]

The size of the data that you want to load into the enclave, in bytes. This value must be a whole-number multiple of the page size.

### -param flProtect [in]

The memory protection to use for the pages that you want to add to the enclave. For a list of memory protection values, see [memory protection constants](/windows/win32/Memory/memory-protection-constants). This value must not include the following constants:

- **PAGE_GUARD**
- **PAGE_NOCACHE**
- **PAGE_WRITECOMBINE**
- **PAGE_NOACCESS**

This value can include the enclave specific constants that the following table describes:

| Constant | Description |
| --- | --- |
| **PAGE_ENCLAVE_THREAD_CONTROL** | The page contains a thread control structure (TCS). |
| **PAGE_ENCLAVE_UNVALIDATED** | The page contents that you supply are excluded from measurement with the EEXTEND instruction of the Intel Software Guard Extensions programming model. |

### -param lpPageInformation [in]

A pointer to information that describes the pages that you want to add to the enclave. The *lpPageInformation* parameter is not used.

### -param dwInfoLength [in]

The length of the structure that the *lpPageInformation* parameter points to, in bytes. This value must be `0`.

### -param lpNumberOfBytesWritten [out]

A pointer to a variable that receives the number of bytes that **LoadEnclaveData** copied into the enclave.

### -param lpEnclaveError [out, optional]

An optional pointer to  a variable that receives an enclave error code that is architecture-specific. The *lpEnclaveError* parameter is not used.

## -returns

If all of the data is loaded into the enclave successfully, the return value is nonzero. Otherwise, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

For a list of common error codes, see [System Error Codes](/windows/win32/Debug/system-error-codes). The following error codes also apply for this function.

| Return code | Description |
|------|--------|
| **ERROR_BAD_LENGTH** | The value of the *dwInfoLength* parameter did not match the value expected based on the value specified for the *lpPageInformation* parameter. |

## -remarks

To initialize the enclave after you load data into the enclave, call [InitializeEnclave](nf-enclaveapi-initializeenclave.md).

**LoadEnclaveData** is only supported enclaves that have the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types.

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[CreateEnclave](nf-enclaveapi-createenclave.md)

[InitializeEnclave](nf-enclaveapi-initializeenclave.md)

[Memory protection constants](/windows/win32/Memory/memory-protection-constants)
