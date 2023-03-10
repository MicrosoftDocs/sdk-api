---
UID: NF:enclaveapi.CallEnclave
title: CallEnclave function (enclaveapi.h)
description: Calls a function within an enclave.
helpviewer_keywords: ["CallEnclave","CallEnclave function","base.callenclave","enclaveapi/CallEnclave"]
old-location: base\callenclave.htm
tech.root: base
ms.assetid: 4C495245-381F-4561-970D-5FCEC105276B
ms.date: 12/05/2018
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
req.lib: Vertdll.lib
req.dll: Vertdll.dll; Api-ms-win-core-enclave-l1-1-0.dll
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
 - Vertdll.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - CallEnclave
---

# CallEnclave function


## -description

Calls a function within an enclave. <b>CallEnclave</b> can also be called within an enclave to call a function outside of the enclave.

## -parameters

### -param lpRoutine [in]

The address of the function that you want to call.

### -param lpParameter [in]

The parameter than you want to pass to the function.

### -param fWaitForThread [in]

<b>TRUE</b> if the call to the specified function should block execution until an idle enclave thread becomes available when no idle enclave thread is available. 
<b>FALSE</b> if the call to the specified function should fail when no idle enclave thread is available. 


This parameter is ignored when you use <b>CallEnclave</b> within an enclave to call a function that is not in any enclave.

### -param lpReturnValue [out]

The return value of the function, if it is called successfully.

## -returns

<b>TRUE</b> if the specified function was called successfully; otherwise <b>FALSE</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-terminateenclave">TerminateEnclave</a>