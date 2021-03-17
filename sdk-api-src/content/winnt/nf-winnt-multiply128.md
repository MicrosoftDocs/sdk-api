---
UID: NF:winnt.Multiply128
title: Multiply128 function (winnt.h)
description: Multiplies two 64-bit integers to produce a 128-bit integer.
helpviewer_keywords: ["Multiply128","Multiply128 function [Windows API]","winnt/Multiply128","winprog.multiply128"]
old-location: winprog\multiply128.htm
tech.root: WinProg
ms.assetid: EB398E5B-1EE8-4BFA-889A-A46094F82B9F
ms.date: 12/05/2018
ms.keywords: Multiply128, Multiply128 function [Windows API], winnt/Multiply128, winprog.multiply128
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
 - Multiply128
 - winnt/Multiply128
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
 - Multiply128
---

# Multiply128 function


## -description

Multiplies two 64-bit integers to produce a 128-bit integer.

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

<a href="/previous-versions/82cxdw50(v=vs.85)">__mul128</a>