---
UID: NF:enclaveapi.TerminateEnclave
title: TerminateEnclave function (enclaveapi.h)
description: Ends the execution of the threads that are running within an enclave.
helpviewer_keywords: ["TerminateEnclave","TerminateEnclave function","base.terminateenclave","enclaveapi/TerminateEnclave"]
old-location: base\terminateenclave.htm
tech.root: base
ms.assetid: D2BAF02F-AE05-43F2-BDB1-013EAF3AC653
ms.date: 02/02/2024
ms.keywords: TerminateEnclave, TerminateEnclave function, base.terminateenclave, enclaveapi/TerminateEnclave
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
 - TerminateEnclave
 - enclaveapi/TerminateEnclave
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
 - vertdll.dll
api_name:
 - TerminateEnclave
---

# TerminateEnclave function

## -description

Ends the execution of the threads that are running within  an enclave.

## -parameters

### -param lpAddress [in]

The base address of the enclave in which to end the execution of the threads.

### -param fWait [in]

`TRUE` if **TerminateEnclave** should not return until all of the threads in the enclave end execution. `FALSE` if **TerminateEnclave** should return immediately.

## -returns

`TRUE` if the function succeeds; otherwise `FALSE`. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[CallEnclave](nf-enclaveapi-callenclave.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
