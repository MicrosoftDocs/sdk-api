---
UID: NF:winnt.MemoryBarrier
title: MemoryBarrier function (winnt.h)
description: Creates a hardware memory barrier (fence) that prevents the CPU from re-ordering read and write operations. It may also prevent the compiler from re-ordering read and write operations.
helpviewer_keywords: ["MemoryBarrier","MemoryBarrier function","base.memorybarrier","winnt/MemoryBarrier"]
old-location: base\memorybarrier.htm
tech.root: backup
ms.assetid: f2c06679-fa2f-4357-ae11-6cec1e50fd8f
ms.date: 12/05/2018
ms.keywords: MemoryBarrier, MemoryBarrier function, base.memorybarrier, winnt/MemoryBarrier
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - MemoryBarrier
 - winnt/MemoryBarrier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MemoryBarrier
---

# MemoryBarrier function


## -description

Creates a hardware memory barrier (fence) that prevents the CPU from re-ordering read and write operations. It may also prevent the compiler from re-ordering read and write operations.



## -remarks

Use this macro or the interlocked functions when the order of memory read and write operations is critical for program operation.

The <b>_ReadBarrier</b>, <b>_WriteBarrier</b>, and <b>_ReadWriteBarrier</b> compiler intrinsics prevent compiler re-ordering only. With Visual Studio 2003, <b>volatile</b> to <b>volatile</b> references are ordered; the compiler will not re-order <b>volatile</b> variable access. With Visual Studio 2005, the compiler also uses acquire semantics for read operations on <b>volatile</b> variables and release semantics for write operations on <b>volatile</b> variables (when supported by the CPU). For more information, see <a href="/windows/desktop/Sync/synchronization-and-multiprocessor-issues">Synchronization and Multiprocessor Issues</a>.

This macro can be called on all processor platforms where Windows is supported, but it  has no effect on some platforms. The definition varies from platform to platform. The following are some definitions of this macro in Winnt.h.


``` syntax

#ifdef _AMD64_
#define MemoryBarrier __faststorefence
#endif

#ifdef _IA64_
#define MemoryBarrier __mf
#endif

// x86

FORCEINLINE
VOID
MemoryBarrier (
    VOID
    )
{
    LONG Barrier;
    __asm {
        xchg Barrier, eax
    }
}
```


## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>
