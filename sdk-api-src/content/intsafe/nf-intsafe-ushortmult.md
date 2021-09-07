---
UID: NF:intsafe.UShortMult
title: UShortMult function (intsafe.h)
description: Multiplies one value of type USHORT by another.
helpviewer_keywords: ["UShortMult","UShortMult function [Windows Shell]","WordMult","_shell_UShortMult","intsafe/UShortMult","shell.UShortMult"]
old-location: shell\UShortMult.htm
tech.root: shell
ms.assetid: ecade442-3272-4886-87e1-057f82f465cf
ms.date: 12/05/2018
ms.keywords: UShortMult, UShortMult function [Windows Shell], WordMult, _shell_UShortMult, intsafe/UShortMult, shell.UShortMult
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
 - UShortMult
 - intsafe/UShortMult
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
 - UShortMult
---

# UShortMult function


## -description

Multiplies one value of type <b>USHORT</b> by another.

## -parameters

### -param usMultiplicand [in]

Type: <b>USHORT</b>

The value to be multiplied by <i>usMultiplier</i>.

### -param usMultiplier [in]

Type: <b>USHORT</b>

The value by which to multiply <i>usMultiplicand</i>.

### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

<b>WordMult</b> is an alias for this function.

