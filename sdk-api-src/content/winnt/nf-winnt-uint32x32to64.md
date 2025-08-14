---
UID: NF:winnt.UInt32x32To64
title: UInt32x32To64 macro (winnt.h)
description: Multiplies two unsigned 32-bit integers, returning an unsigned 64-bit integer result.
helpviewer_keywords: ["UInt32x32To64","UInt32x32To64 macro [Windows API]","_win32_uint32x32to64","winnt/UInt32x32To64","winprog.uint32x32to64"]
old-location: winprog\uint32x32to64.htm
tech.root: WinProg
ms.assetid: 369e0574-df8b-4e65-bbba-7a7961caebe7
ms.date: 07/01/2025
ms.keywords: UInt32x32To64, UInt32x32To64 macro [Windows API], _win32_uint32x32to64, winnt/UInt32x32To64, winprog.uint32x32to64
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
 - UInt32x32To64
 - winnt/UInt32x32To64
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
 - UInt32x32To64
---

# UInt32x32To64 macro

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

Multiplies two unsigned 32-bit integers, returning an unsigned 64-bit integer result. The function performs optimally on 32-bit Windows.

## -parameters

### -param a [in]

The first unsigned 32-bit integer for the multiplication operation.

### -param b [in]

The second unsigned 32-bit integer for the multiplication operation.

## -remarks

This function is implemented on all platforms by optimal inline code: a single multiply instruction that returns a 64-bit result.

Please note that the function's return value is a 64-bit value, not a 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-int32x32to64">Int32x32To64</a>



<a href="/windows/desktop/WinProg/large-integers">Large Integers</a>
