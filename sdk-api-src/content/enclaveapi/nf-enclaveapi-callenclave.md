---
UID: NF:enclaveapi.CallEnclave
title: CallEnclave function (enclaveapi.h)
description: Calls a function within an enclave.
helpviewer_keywords: ["CallEnclave","CallEnclave function","base.callenclave","enclaveapi/CallEnclave"]
old-location: base\callenclave.htm
tech.root: base
ms.assetid: 4C495245-381F-4561-970D-5FCEC105276B
ms.date: 02/02/2024
ms.keywords: CallEnclave, CallEnclave function, base.callenclave, enclaveapi/CallEnclave
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
req.lib: Kernel32.lib
req.dll: Api-ms-win-core-enclave-l1-1-0.dll; Kernel32.dll; KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CallEnclave
 - enclaveapi/CallEnclave
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
 - KernelBase.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - CallEnclave
---

# CallEnclave function

## -description

Calls a function within an enclave. **CallEnclave** can also be called within an enclave to call a function outside of the enclave.

## -parameters

### -param lpRoutine [in]

The address of the function that you want to call.

### -param lpParameter [in]

The parameter than you want to pass to the function.

### -param fWaitForThread [in]

`TRUE` if the call to the specified function should block execution until an idle enclave thread becomes available when no idle enclave thread is available. `FALSE` if the call to the specified function should fail when no idle enclave thread is available.

This parameter is ignored when you use **CallEnclave** within an enclave to call a function that is not in any enclave.

### -param lpReturnValue [out]

The return value of the function, if it is called successfully.

## -returns

`TRUE` if the specified function was called successfully; otherwise `FALSE`. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[TerminateEnclave](nf-enclaveapi-terminateenclave.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
