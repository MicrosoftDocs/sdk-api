---
UID: NF:winnt.Int64ShrlMod32
title: Int64ShrlMod32 macro (winnt.h)
description: Performs a right logical shift operation on an unsigned 64-bit integer value. The function provides improved shifting code for right logical shifts where the shift count is in the range 0-31.
helpviewer_keywords: ["Int64ShrlMod32","Int64ShrlMod32 macro [Windows API]","_win32_int64shrlmod32","winnt/Int64ShrlMod32","winprog.int64shrlmod32"]
old-location: winprog\int64shrlmod32.htm
tech.root: WinProg
ms.assetid: 95ce281a-92b1-4c9b-a345-6b50f0285d65
ms.date: 07/01/2025
ms.keywords: Int64ShrlMod32, Int64ShrlMod32 macro [Windows API], _win32_int64shrlmod32, winnt/Int64ShrlMod32, winprog.int64shrlmod32
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
 - Int64ShrlMod32
 - winnt/Int64ShrlMod32
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
 - Int64ShrlMod32
---

# Int64ShrlMod32 macro

## -syntax

```cpp
ULONGLONG Int64ShrlMod32(
  [in]  ULONGLONG a,
  [in]  DWORD b
);
```

## -returns

Type: **ULONGLONG**

The return value is the unsigned 64-bit integer result of the right logical shift operation.


## -description

Performs a right logical shift operation on an unsigned 64-bit integer value. The function provides improved shifting code for right logical shifts where the shift count is in the range 0-31.

## -parameters

### -param a [in]

The unsigned 64-bit integer to be shifted.

### -param b [in]

The shift count in the range 0-31.

## -remarks

The shift count is the number of bit positions that the value's bits move.

In a right logical shift operation on an unsigned value, the value's bits move to the right, and vacated bits on the left side of the value are set to zero.

A compiler can generate optimal code for a right logical shift operation when the shift count is a constant. However, if the shift count is a variable whose range of values is unknown, the compiler must assume the worst case, leading to non-optimal code: code that calls a subroutine, or code that is inline but branches. By restricting the shift count to the range 0-31, the 
<b>Int64ShrlMod32</b> function lets the compiler generate optimal or near-optimal code.

<div class="alert"><b>Note</b>  The 
<b>Int64ShrlMod32</b> function's <i>Value</i> parameter and return value are 64-bit values, not 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structures.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-int64shllmod32">Int64ShllMod32</a>



<a href="/windows/desktop/api/winnt/nf-winnt-int64shramod32">Int64ShraMod32</a>



<a href="/windows/desktop/WinProg/large-integers">Large Integers</a>
