---
UID: NF:intsafe.IntPtrToULongLong
title: IntPtrToULongLong function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type ULONGLONG.
helpviewer_keywords: ["IntPtrToULongLong","IntPtrToULongLong function [Windows Shell]","UIntPtrToInt64","_shell_IntPtrToULongLong","intsafe/IntPtrToULongLong","shell.IntPtrToULongLong"]
old-location: shell\IntPtrToULongLong.htm
tech.root: shell
ms.assetid: 81358f7f-9e78-469a-889e-85fa93bd1eac
ms.date: 12/05/2018
ms.keywords: IntPtrToULongLong, IntPtrToULongLong function [Windows Shell], UIntPtrToInt64, _shell_IntPtrToULongLong, intsafe/IntPtrToULongLong, shell.IntPtrToULongLong
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
 - IntPtrToULongLong
 - intsafe/IntPtrToULongLong
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
 - IntPtrToULongLong
---

# IntPtrToULongLong function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>ULONGLONG</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT_PTR</b>

The value to be converted.

### -param pullResult [out]

Type: <b>ULONGLONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks, and to do so with minimal impact on performance.

<b>UIntPtrToInt64</b> is an alias for this function.

