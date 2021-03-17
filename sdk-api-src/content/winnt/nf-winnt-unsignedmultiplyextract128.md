---
UID: NF:winnt.UnsignedMultiplyExtract128
title: UnsignedMultiplyExtract128 function (winnt.h)
description: Multiplies two unsigned 64-bit integers to produce an unsigned 128-bit integer, shifts the product to the right by the specified number of bits, and returns the low 64 bits of the result.
helpviewer_keywords: ["UnsignedMultiplyExtract128","UnsignedMultiplyExtract128 function [Windows API]","winnt/UnsignedMultiplyExtract128","winprog.unsignedmultiplyextract128"]
old-location: winprog\unsignedmultiplyextract128.htm
tech.root: WinProg
ms.assetid: 93a2550d-b95a-4206-95a6-3412d9b38f37
ms.date: 12/05/2018
ms.keywords: UnsignedMultiplyExtract128, UnsignedMultiplyExtract128 function [Windows API], winnt/UnsignedMultiplyExtract128, winprog.unsignedmultiplyextract128
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
 - UnsignedMultiplyExtract128
 - winnt/UnsignedMultiplyExtract128
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
 - UnsignedMultiplyExtract128
---

# UnsignedMultiplyExtract128 function


## -description

Multiplies two unsigned 64-bit integers to produce an unsigned 128-bit integer, shifts the product to the right by the specified number of bits, and returns the low 64 bits of the result.

## -parameters

### -param Multiplier [in]

The first integer.

### -param Multiplicand [in]

The second integer.

### -param Shift [in]

The number of bits to shift.

## -returns

The low 64 bits of the result.

