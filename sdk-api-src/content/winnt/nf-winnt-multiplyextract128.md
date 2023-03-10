---
UID: NF:winnt.MultiplyExtract128
title: MultiplyExtract128 function (winnt.h)
description: Multiplies two 64-bit integers to produce a 128-bit integer, shifts the product to the right by the specified number of bits, and returns the low 64 bits of the result.
helpviewer_keywords: ["MultiplyExtract128","MultiplyExtract128 function [Windows API]","winnt/MultiplyExtract128","winprog.multiplyextract128"]
old-location: winprog\multiplyextract128.htm
tech.root: WinProg
ms.assetid: 7b178c3e-076c-472b-8205-3a52a0e6a7b5
ms.date: 12/05/2018
ms.keywords: MultiplyExtract128, MultiplyExtract128 function [Windows API], winnt/MultiplyExtract128, winprog.multiplyextract128
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
 - MultiplyExtract128
 - winnt/MultiplyExtract128
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
 - MultiplyExtract128
---

# MultiplyExtract128 function


## -description

Multiplies two 64-bit integers to produce a 128-bit integer, shifts the product to the right by the specified number of bits, and returns the low 64 bits of the result.

## -parameters

### -param Multiplier [in]

The first integer.

### -param Multiplicand [in]

The second integer.

### -param Shift [in]

The number of bits to shift.

## -returns

The low 64 bits of the result.

