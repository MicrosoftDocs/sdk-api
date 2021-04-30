---
UID: NF:winnt.UnsignedMultiply128
title: UnsignedMultiply128 function (winnt.h)
description: Multiplies two unsigned 64-bit integers to produce an unsigned 128-bit integer.
helpviewer_keywords: ["UnsignedMultiply128","UnsignedMultiply128 function [Windows API]","winnt/UnsignedMultiply128","winprog.unsignedmultiply128"]
old-location: winprog\unsignedmultiply128.htm
tech.root: WinProg
ms.assetid: C9F8D594-3E25-4494-835F-A873045FE83F
ms.date: 12/05/2018
ms.keywords: UnsignedMultiply128, UnsignedMultiply128 function [Windows API], winnt/UnsignedMultiply128, winprog.unsignedmultiply128
req.header: winnt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnsignedMultiply128
 - winnt/UnsignedMultiply128
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
 - UnsignedMultiply128
---

# UnsignedMultiply128 function


## -description

Multiplies two unsigned 64-bit integers to produce an unsigned 128-bit integer.

## -parameters

### -param Multiplier [in]

The first integer.

### -param Multiplicand [in]

The second integer.

### -param HighProduct [out]

The high 64 bits of the product.

## -returns

The low 64 bits of the product.

## -see-also

<a href="/previous-versions/3dayytw9(v=vs.85)">_umu128</a>