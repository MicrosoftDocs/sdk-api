---
UID: NF:winnt.RtlUnwind2
title: RtlUnwind2 function (winnt.h)
description: Initiates an unwind of procedure call frames. (RtlUnwind2)
helpviewer_keywords: ["RtlUnwind2","RtlUnwind2 function","base.rtlunwind2","winnt/RtlUnwind2"]
old-location: base\rtlunwind2.htm
tech.root: Debug
ms.assetid: 8015d070-51b9-49d4-b760-c9faaeba2cd0
ms.date: 12/05/2018
ms.keywords: RtlUnwind2, RtlUnwind2 function, base.rtlunwind2, winnt/RtlUnwind2
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Intel Itanium edition of Windows Server 2003 or     Windows XP
ms.custom: 19H1
f1_keywords:
 - RtlUnwind2
 - winnt/RtlUnwind2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - RtlUnwind2
---

# RtlUnwind2 function


## -description

Initiates an unwind of 
   procedure call frames.

## -parameters

### -param TargetFrame [in, optional]

A pointer to the call frame that is the target of the unwind. If this parameter is 
      <b>NULL</b>, the function performs an exit unwind.

### -param TargetIp [in, optional]

The continuation address of the unwind. This parameter is ignored if <i>TargetFrame</i> 
      is <b>NULL</b>.

### -param ExceptionRecord [in, optional]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> 
      structure.

### -param ReturnValue [in]

A value to be placed in the integer function return register before continuing execution.

### -param ContextRecord [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that stores context 
     during the unwind operation.

## -returns

This function does not return a value.

## -remarks

The <b>FRAME_POINTERS</b> structure is defined as follows:


```cpp
typedef struct _FRAME_POINTERS {
    ULONGLONG MemoryStackFp;
    ULONGLONG BackingStoreFp;
} FRAME_POINTERS, *PFRAME_POINTERS;
```

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a>
