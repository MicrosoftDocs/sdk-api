---
UID: NF:intsafe.ULongPtrMult
title: ULongPtrMult function (intsafe.h)
description: Multiplies one value of type ULONG_PTR by another.
helpviewer_keywords: ["ULongPtrMult","ULongPtrMult function [Windows Shell]","_shell_ULongPtrMult","intsafe/ULongPtrMult","shell.ULongPtrMult"]
old-location: shell\ULongPtrMult.htm
tech.root: shell
ms.assetid: e3ee5794-b872-4286-b4f3-1c5cab0e42a8
ms.date: 12/05/2018
ms.keywords: ULongPtrMult, ULongPtrMult function [Windows Shell], _shell_ULongPtrMult, intsafe/ULongPtrMult, shell.ULongPtrMult
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
 - ULongPtrMult
 - intsafe/ULongPtrMult
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
 - ULongPtrMult
---

# ULongPtrMult function


## -description

Multiplies one value of type <b>ULONG_PTR</b> by another.

## -parameters

### -param ulMultiplicand [in]

Type: <b>ULONG_PTR</b>

The value to be multiplied by <i>ulMultiplier</i>.

### -param ulMultiplier [in]

Type: <b>ULONG_PTR</b>

The value by which to multiply <i>ulMultiplicand</i>.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

