---
UID: NF:intsafe.ULongPtrToULong
title: ULongPtrToULong function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type ULONG.
helpviewer_keywords: ["DWordPtrToDWord","DWordPtrToULong","SIZETToDWord","SIZETToULong","ULongPtrToDWord","ULongPtrToULong","ULongPtrToULong function [Windows Shell]","_shell_ULongPtrToULong","intsafe/ULongPtrToULong","shell.ULongPtrToULong"]
old-location: shell\ULongPtrToULong.htm
tech.root: shell
ms.assetid: 7cae7414-055c-4362-8023-71ff9db20cbb
ms.date: 12/05/2018
ms.keywords: DWordPtrToDWord, DWordPtrToULong, SIZETToDWord, SIZETToULong, ULongPtrToDWord, ULongPtrToULong, ULongPtrToULong function [Windows Shell], _shell_ULongPtrToULong, intsafe/ULongPtrToULong, shell.ULongPtrToULong
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
 - ULongPtrToULong
 - intsafe/ULongPtrToULong
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
 - ULongPtrToULong
---

# ULongPtrToULong function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>ULONG</b>.

## -parameters

### -param ulOperand [in]

Type: <b>ULONG_PTR</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordPtrToULong</b> is an alias for this function.

<b>SIZETToULong</b> is an alias for this function.

<b>ULongPtrToDWord</b> is an alias for this function.

<b>DWordPtrToDWord</b> is an alias for this function.

<b>SIZETToDWord</b> is an alias for this function.

