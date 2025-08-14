---
UID: NF:enclaveapi.DeleteEnclave
title: DeleteEnclave function (enclaveapi.h)
description: Deletes the specified enclave.
helpviewer_keywords: ["DeleteEnclave","DeleteEnclave function","base.deleteenclave","enclaveapi/DeleteEnclave"]
old-location: base\deleteenclave.htm
tech.root: base
ms.assetid: 04FCD129-3A3B-40EA-AD62-01C674CF2E61
ms.date: 02/02/2024
ms.keywords: DeleteEnclave, DeleteEnclave function, base.deleteenclave, enclaveapi/DeleteEnclave
req.header: enclaveapi.h
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
req.lib: onecore.lib
req.dll: kernel32.dll; Api-ms-win-core-enclave-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeleteEnclave
 - enclaveapi/DeleteEnclave
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-enclave-l1-1-1.dll
 - kernel32.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - DeleteEnclave
---

# DeleteEnclave function

## -description

Deletes the specified enclave.

## -parameters

### -param lpAddress [in]

The base address of the enclave that you want to delete.

## -returns

`TRUE` if the enclave was deleted successfully; otherwise `FALSE`. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

For a list of common error codes, see [System Error Codes](/windows/win32/Debug/system-error-codes). The following error codes also apply for this function.

| Return code | Description |
|-------------|-------------|
| **ERROR_ENCLAVE_NOT_TERMINATED** | The execution of threads running with the enclave was not ended, because either [TerminateEnclave](nf-enclaveapi-terminateenclave.md) was not called, or the execution of the threads has not yet ended in response to an earlier call to **TerminateEnclave**. |

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[TerminateEnclave](nf-enclaveapi-terminateenclave.md)

[CreateEnclave](nf-enclaveapi-createenclave.md)
