---
UID: NF:winnt.Int64ShllMod32
title: Int64ShllMod32 macro (winnt.h)
description: Performs a left logical shift operation on an unsigned 64-bit integer value. The function provides improved shifting code for left logical shifts where the shift count is in the range 0-31.
helpviewer_keywords: ["Int64ShllMod32","Int64ShllMod32 macro [Windows API]","_win32_int64shllmod32","winnt/Int64ShllMod32","winprog.int64shllmod32"]
old-location: winprog\int64shllmod32.htm
tech.root: WinProg
ms.assetid: fe79b0c4-3316-4b05-b088-0d4b45586430
ms.date: 07/01/2025
ms.keywords: Int64ShllMod32, Int64ShllMod32 macro [Windows API], _win32_int64shllmod32, winnt/Int64ShllMod32, winprog.int64shllmod32
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - Int64ShllMod32
 - winnt/Int64ShllMod32
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
 - Int64ShllMod32
---

# Int64ShllMod32 macro

## -syntax

```cpp
ULONGLONG Int64ShllMod32(
  [in]  ULONGLONG a,
  [in]  DWORD b
);
```

## -returns

Type: **ULONGLONG**

The return value is the unsigned 64-bit integer result of the left logical shift operation.


## -description

Performs a left logical shift operation on an unsigned 64-bit integer value. The function provides improved shifting code for left logical shifts where the shift count is in the range 0-31.

## -parameters

### -param a [in]

The unsigned 64-bit integer to be shifted.

### -param b [in]

The shift count in the range 0-31.

## -remarks

The shift count is the number of bit positions that the value's bits move.

In a left logical shift operation on an unsigned value, the value's bits move to the left, and vacated bits on the right side of the value are set to zero.

A compiler can generate optimal code for a left logical shift operation when the shift count is a constant. However, if the shift count is a variable whose range of values is unknown, the compiler must assume the worst case, leading to non-optimal code: code that calls a subroutine, or code that is inline but branches. By restricting the shift count to the range 0-31, the 
<b>Int64ShllMod32</b> function lets the compiler generate optimal or near-optimal code.

Please note that the 
<b>Int64ShllMod32</b> function's <i>Value</i> parameter and return value are 64-bit values, not 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structures.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-int64shramod32">Int64ShraMod32</a>



<a href="/windows/desktop/api/winnt/nf-winnt-int64shrlmod32">Int64ShrlMod32</a>



<a href="/windows/desktop/WinProg/large-integers">Large Integers</a>
