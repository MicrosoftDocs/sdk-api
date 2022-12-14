---
UID: NF:intsafe.IntPtrToLong
title: IntPtrToLong function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type LONG.
helpviewer_keywords: ["IntPtrToLong","IntPtrToLong function [Windows Shell]","_shell_IntPtrToLong","intsafe/IntPtrToLong","shell.IntPtrToLong"]
old-location: shell\IntPtrToLong.htm
tech.root: shell
ms.assetid: 43ccfd9b-6bef-4870-ad7a-f207443cf5cf
ms.date: 12/05/2018
ms.keywords: IntPtrToLong, IntPtrToLong function [Windows Shell], _shell_IntPtrToLong, intsafe/IntPtrToLong, shell.IntPtrToLong
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
 - IntPtrToLong
 - intsafe/IntPtrToLong
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
 - IntPtrToLong
---

# IntPtrToLong function


## -description

Converts  a value of type <b>INT_PTR</b> to a value of type <b>LONG</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT_PTR</b>

The value to be converted.

### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

