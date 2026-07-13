---
UID: NF:winbase.InterlockedExchangeSubtract
title: InterlockedExchangeSubtract function (winbase.h)
description: Performs an atomic subtraction of two values.
helpviewer_keywords: ["InterlockedExchangeSubtract","InterlockedExchangeSubtract function","base.interlockedexchangesubtract","winbase/InterlockedExchangeSubtract"]
old-location: base\interlockedexchangesubtract.htm
tech.root: backup
ms.assetid: 9917323D-38C4-446E-B59A-52493A6020ED
ms.date: 12/05/2018
ms.keywords: InterlockedExchangeSubtract, InterlockedExchangeSubtract function, base.interlockedexchangesubtract, winbase/InterlockedExchangeSubtract
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedExchangeSubtract
 - winbase/InterlockedExchangeSubtract
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - InterlockedExchangeSubtract
---

# InterlockedExchangeSubtract function


## -description

Performs an atomic subtraction of two values.

## -parameters

### -param Addend [in, out]

A pointer to a variable. The value of this variable is replaced with the result of the operation.

### -param Value [in]

The value to be subtracted from the variable pointed to by the <i>Addend</i> parameter.

## -returns

The function returns the initial value of  the <i>Addend</i> parameter.

## -remarks

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange">InterlockedExchange</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer">InterlockedExchangePointer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>