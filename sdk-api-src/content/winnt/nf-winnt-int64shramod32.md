---
UID: NF:winnt.Int64ShraMod32
title: Int64ShraMod32 macro (winnt.h)
description: Performs a right arithmetic shift operation on a signed 64-bit integer value. The function provides improved shifting code for right arithmetic shifts where the shift count is in the range 0-31.
helpviewer_keywords: ["Int64ShraMod32","Int64ShraMod32 macro [Windows API]","_win32_int64shramod32","winnt/Int64ShraMod32","winprog.int64shramod32"]
old-location: winprog\int64shramod32.htm
tech.root: WinProg
ms.assetid: 69de2eb7-2cbe-48db-935b-b3d2c41f4e86
ms.date: 07/01/2025
ms.keywords: Int64ShraMod32, Int64ShraMod32 macro [Windows API], _win32_int64shramod32, winnt/Int64ShraMod32, winprog.int64shramod32
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
 - Int64ShraMod32
 - winnt/Int64ShraMod32
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
 - Int64ShraMod32
---

# Int64ShraMod32 macro

## -syntax

```cpp
LONGLONG Int64ShraMod32(
  [in]  LONGLONG a,
  [in]  DWORD b
);
```

## -returns

Type: **LONGLONG**

The return value is the signed 64-bit integer result of the right arithmetic shift operation.


## -description

Performs a right arithmetic shift operation on a signed 64-bit integer value. The function provides improved shifting code for right arithmetic shifts where the shift count is in the range 0-31.

## -parameters

### -param a [in]

The signed 64-bit integer to be shifted.

### -param b [in]

The shift count in the range 0-31.

## -remarks

The shift count is the number of bit positions that the value's bits move.

In a right arithmetic shift operation on a signed value, the value's bits move to the right, and vacated bits on the left side of the value are set to the value of the sign bit.

A compiler can generate optimal code for a right arithmetic shift operation when the shift count is a constant. However, if the shift count is a variable whose range of values is unknown, the compiler must assume the worst case, leading to non-optimal code: code that calls a subroutine, or code that is inline but branches. By restricting the shift count to the range 0-31, the 
<b>Int64ShraMod32</b> function lets the compiler generate optimal or near-optimal code.

Please note that the 
<b>Int64ShraMod32</b> function's <i>Value</i> parameter and return value are 64-bit values, not 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structures.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-int64shllmod32">Int64ShllMod32</a>



<a href="/windows/desktop/api/winnt/nf-winnt-int64shrlmod32">Int64ShrlMod32</a>



<a href="/windows/desktop/WinProg/large-integers">Large Integers</a>
