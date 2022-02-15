---
UID: NF:intsafe.ULongMult
title: ULongMult function (intsafe.h)
description: Multiplies one value of type ULONG by another.
helpviewer_keywords: ["DWordMult","ULongMult","ULongMult function [Windows Shell]","_shell_ULongMult","intsafe/ULongMult","shell.ULongMult"]
old-location: shell\ULongMult.htm
tech.root: shell
ms.assetid: 79710ade-498d-4cd7-ae6e-552a8e787193
ms.date: 12/05/2018
ms.keywords: DWordMult, ULongMult, ULongMult function [Windows Shell], _shell_ULongMult, intsafe/ULongMult, shell.ULongMult
req.header: intsafe.h
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
 - ULongMult
 - intsafe/ULongMult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - ULongMult
---

# ULongMult function


## -description

Multiplies one value of type <b>ULONG</b> by another.

## -parameters

### -param ulMultiplicand [in]

Type: <b>ULONG</b>

The value to be multiplied by <i>ulMultiplier</i>.

### -param ulMultiplier [in]

Type: <b>ULONG</b>

The value by which to multiply <i>ulMultiplicand</i>.

### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

<b>DWordMult</b> is an alias for this function.

