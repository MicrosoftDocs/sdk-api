---
UID: NF:winnt.Int32x32To64
title: Int32x32To64 macro (winnt.h)
description: Multiplies two signed 32-bit integers, returning a signed 64-bit integer result.
helpviewer_keywords: ["Int32x32To64","Int32x32To64 macro [Windows API]","_win32_int32x32to64","winnt/Int32x32To64","winprog.int32x32to64"]
old-location: winprog\int32x32to64.htm
tech.root: WinProg
ms.assetid: 5c0caf42-2a2f-4eae-b0be-e8bb1b87dd9d
ms.date: 07/01/2025
ms.keywords: Int32x32To64, Int32x32To64 macro [Windows API], _win32_int32x32to64, winnt/Int32x32To64, winprog.int32x32to64
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Int32x32To64
 - winnt/Int32x32To64
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
 - Int32x32To64
---

# Int32x32To64 macro

## -syntax

```cpp
LONGLONG Int32x32To64(
  [in]  LONG a,
  [in]  LONG b
);
```

## -returns

Type: **LONGLONG**

The return value is the signed 64-bit integer result of the multiplication operation.


## -description

Multiplies two signed 32-bit integers, returning a signed 64-bit integer result. The function performs optimally on 32-bit Windows.

## -parameters

### -param a [in]

The first signed 32-bit integer for the multiplication operation.

### -param b [in]

The second signed 32-bit integer for the multiplication operation.

## -remarks

This function is implemented on all platforms by optimal inline code: a single multiply instruction that returns a 64-bit result.

Please note that the function's return value is a 64-bit value, not a 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure.

## -see-also

<a href="/windows/desktop/WinProg/large-integers">Large Integers</a>



<a href="/windows/desktop/api/winnt/nf-winnt-uint32x32to64">UInt32x32To64</a>
