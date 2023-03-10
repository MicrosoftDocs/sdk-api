---
UID: NF:intsafe.UIntMult
title: UIntMult function (intsafe.h)
description: Multiplies one value of type UINT by another.
helpviewer_keywords: ["UIntMult","UIntMult function [Windows Shell]","_shell_UIntMult","intsafe/UIntMult","shell.UIntMult"]
old-location: shell\UIntMult.htm
tech.root: shell
ms.assetid: c469417c-c774-4946-b873-cc2845417655
ms.date: 12/05/2018
ms.keywords: UIntMult, UIntMult function [Windows Shell], _shell_UIntMult, intsafe/UIntMult, shell.UIntMult
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
 - UIntMult
 - intsafe/UIntMult
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
 - UIntMult
---

# UIntMult function


## -description

Multiplies one value of type <b>UINT</b> by another.

## -parameters

### -param uMultiplicand [in]

Type: <b>UINT</b>

The value to be multiplied by <i>uMultiplier</i>.

### -param uMultiplier [in]

Type: <b>UINT</b>

The value by which to multiply <i>uMultiplicand</i>.

### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

