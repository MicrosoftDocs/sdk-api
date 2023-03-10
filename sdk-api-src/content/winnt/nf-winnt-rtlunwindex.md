---
UID: NF:winnt.RtlUnwindEx
title: RtlUnwindEx function (winnt.h)
description: Initiates an unwind of procedure call frames.
helpviewer_keywords: ["RtlUnwindEx","RtlUnwindEx function","base.rtlunwindex","winnt/RtlUnwindEx"]
old-location: base\rtlunwindex.htm
tech.root: Debug
ms.assetid: 3d2d8778-311e-4cc1-b280-4f83ab457755
ms.date: 12/05/2018
ms.keywords: RtlUnwindEx, RtlUnwindEx function, base.rtlunwindex, winnt/RtlUnwindEx
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
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
ms.custom: 19H1
f1_keywords:
 - RtlUnwindEx
 - winnt/RtlUnwindEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-rtlsupport-l1-1-0.dll
 - ntdll.dll
 - API-MS-Win-Core-rtlsupport-l1-2-0.dll
 - ntoskrnl.exe
api_name:
 - RtlUnwindEx
---

# RtlUnwindEx function


## -description

Initiates an unwind of 
   procedure call frames.

## -parameters

### -param TargetFrame [in, optional]

A pointer to the call frame that is the target of the unwind. If this parameter is <b>NULL</b>, the function 
      performs an exit unwind.

### -param TargetIp [in, optional]

The continuation address of the unwind. This parameter is ignored if <i>TargetFrame</i> is 
      <b>NULL</b>.

### -param ExceptionRecord [in, optional]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> structure.

### -param ReturnValue [in]

A value to be placed in the integer function return register before continuing execution.

### -param ContextRecord [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that stores context 
      during the unwind operation.

### -param HistoryTable [in, optional]

A pointer to the unwind history table. This structure is processor specific. For definitions of this 
      structure, see Winternl.h.

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