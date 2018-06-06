---
UID: NF:winbase.InterlockedExchangeSubtract
title: InterlockedExchangeSubtract function
author: windows-sdk-content
description: Performs an atomic subtraction of two values.
old-location: base\interlockedexchangesubtract.htm
old-project: Sync
ms.assetid: 9917323D-38C4-446E-B59A-52493A6020ED
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: InterlockedExchangeSubtract, InterlockedExchangeSubtract function, base.interlockedexchangesubtract, winbase/InterlockedExchangeSubtract
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - InterlockedExchangeSubtract
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547853">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547892">InterlockedExchange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547903">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547904">InterlockedExchangePointer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

