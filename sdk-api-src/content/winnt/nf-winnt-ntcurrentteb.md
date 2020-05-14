---
UID: NF:winnt.NtCurrentTeb
title: NtCurrentTeb function (winnt.h)
description: The NtCurrentTeb routine returns a pointer to the Thread Environment Block (TEB) of the current thread.helpviewer_keywords: ["NtCurrentTeb","NtCurrentTeb routine [Kernel-Mode Driver Architecture]","kernel.ntcurrentteb","winnt/NtCurrentTeb"]
old-location: kernel\ntcurrentteb.htm
tech.root: Kernel
ms.assetid: EB68E76F-F838-40B7-AD23-5897321F354F
ms.date: 12/05/2018
ms.keywords: NtCurrentTeb, NtCurrentTeb routine [Kernel-Mode Driver Architecture], kernel.ntcurrentteb, winnt/NtCurrentTeb
f1_keywords:
- winnt/NtCurrentTeb
dev_langs:
- c++
req.header: winnt.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winnt.h
api_name:
- NtCurrentTeb
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NtCurrentTeb function


## -description


The <b>NtCurrentTeb</b> routine returns a pointer to the Thread Environment Block (<a href="https://docs.microsoft.com/windows/desktop/api/winternl/ns-winternl-teb">TEB</a>) of the current thread. 


## -parameters








## -returns



A pointer to the thread environment block of the current thread. 




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/ntxxx-routines">NtXxx Routines</a>
 

 

