---
UID: NF:aux_ulib.AuxUlibIsDLLSynchronizationHeld
title: AuxUlibIsDLLSynchronizationHeld function (aux_ulib.h)
description: Determines whether the caller is holding a synchronization primitive.
old-location: winprog\auxulibisdllsynchronizationheld.htm
tech.root: DevNotes
ms.assetid: fa2adb90-757c-4796-9842-e1f1a16d46fa
ms.date: 12/05/2018
ms.keywords: AuxUlibIsDLLSynchronizationHeld, AuxUlibIsDLLSynchronizationHeld function [Windows API], aux_ulib/AuxUlibIsDLLSynchronizationHeld, winprog.auxulibisdllsynchronizationheld
f1_keywords:
- aux_ulib/AuxUlibIsDLLSynchronizationHeld
dev_langs:
- c++
req.header: aux_ulib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Aux_ulib.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Aux_ulib.lib
api_name:
- AuxUlibIsDLLSynchronizationHeld
targetos: Windows
req.typenames: 
req.redist: Windows Auxiliary API library version 2.0
ms.custom: 19H1
---

# AuxUlibIsDLLSynchronizationHeld function


## -description


Determines whether the caller is holding a synchronization primitive. This information can be used to avoid operations that could potentially lead to deadlocks.


## -parameters




### -param SynchronizationHeld [out]

Indicates whether the caller is holding a synchronization primitive.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



You must call the <a href="https://docs.microsoft.com/windows/desktop/api/aux_ulib/nf-aux_ulib-auxulibinitialize">AuxUlibInitialize</a> function before calling this function.



