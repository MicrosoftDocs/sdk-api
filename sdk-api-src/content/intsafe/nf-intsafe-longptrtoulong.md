---
UID: NF:intsafe.LongPtrToULong
title: LongPtrToULong function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type ULONG.
helpviewer_keywords: ["LongPtrToDWord","LongPtrToULong","LongPtrToULong function [Windows Shell]","SSIZETToDWord","SSIZETToUIntPtr","SSIZETToULong","_shell_LongPtrToULong","intsafe/LongPtrToULong","shell.LongPtrToULong"]
old-location: shell\LongPtrToULong.htm
tech.root: shell
ms.assetid: fa263baa-e254-4ef4-8537-5722f6925da6
ms.date: 12/05/2018
ms.keywords: LongPtrToDWord, LongPtrToULong, LongPtrToULong function [Windows Shell], SSIZETToDWord, SSIZETToUIntPtr, SSIZETToULong, _shell_LongPtrToULong, intsafe/LongPtrToULong, shell.LongPtrToULong
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
 - LongPtrToULong
 - intsafe/LongPtrToULong
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
 - LongPtrToULong
---

# LongPtrToULong function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>ULONG</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG_PTR</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SSIZETToULong</b> is an alias for this function.

<b>SSIZETToUIntPtr</b> is an alias for this function.

<b>SSIZETToDWord</b> is an alias for this function.

<b>LongPtrToDWord</b> is an alias for this function.

