---
UID: NF:winbase.InterlockedExchangeSubtract
title: InterlockedExchangeSubtract function (winbase.h)
description: Performs an atomic subtraction of two values.helpviewer_keywords: ["InterlockedExchangeSubtract","InterlockedExchangeSubtract function","base.interlockedexchangesubtract","winbase/InterlockedExchangeSubtract"]
old-location: base\interlockedexchangesubtract.htm
tech.root: Sync
ms.assetid: 9917323D-38C4-446E-B59A-52493A6020ED
ms.date: 12/05/2018
ms.keywords: InterlockedExchangeSubtract, InterlockedExchangeSubtract function, base.interlockedexchangesubtract, winbase/InterlockedExchangeSubtract
f1_keywords:
- winbase/InterlockedExchangeSubtract
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinBase.h
api_name:
- InterlockedExchangeSubtract
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="https://docs.microsoft.com/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="https://docs.microsoft.com/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange</a>



<a href="https://docs.microsoft.com/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAdd</a>



<a href="https://docs.microsoft.com/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangePointer</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

