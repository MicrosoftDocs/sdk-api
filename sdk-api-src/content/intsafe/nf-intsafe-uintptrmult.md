---
UID: NF:intsafe.UIntPtrMult
title: UIntPtrMult function (intsafe.h)
description: Multiplies one value of type UINT_PTR by another.
helpviewer_keywords: ["UIntPtrMult","UIntPtrMult function [Windows Shell]","_shell_UIntPtrMult","intsafe/UIntPtrMult","shell.UIntPtrMult"]
old-location: shell\UIntPtrMult.htm
tech.root: shell
ms.assetid: c34708d1-50e8-47dd-ac79-cfef24ce6060
ms.date: 12/05/2018
ms.keywords: UIntPtrMult, UIntPtrMult function [Windows Shell], _shell_UIntPtrMult, intsafe/UIntPtrMult, shell.UIntPtrMult
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
 - UIntPtrMult
 - intsafe/UIntPtrMult
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
 - UIntPtrMult
---

# UIntPtrMult function


## -description

Multiplies one value of type <b>UINT_PTR</b> by another.

## -parameters

### -param uMultiplicand [in]

Type: <b>UINT_PTR</b>

The value to be multiplied by <i>uMultiplier</i>.

### -param uMultiplier [in]

Type: <b>UINT_PTR</b>

The value by which to multiply <i>uMultiplicand</i>.

### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

