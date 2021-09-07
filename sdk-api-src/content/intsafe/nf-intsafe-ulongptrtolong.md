---
UID: NF:intsafe.ULongPtrToLong
title: ULongPtrToLong function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type LONG.
helpviewer_keywords: ["DWordPtrToLong","SIZETToLong","ULongPtrToLong","ULongPtrToLong function [Windows Shell]","_shell_ULongPtrToLong","intsafe/ULongPtrToLong","shell.ULongPtrToLong"]
old-location: shell\ULongPtrToLong.htm
tech.root: shell
ms.assetid: 8f3f7cac-7dd4-4fe2-9415-082a24f14ba3
ms.date: 12/05/2018
ms.keywords: DWordPtrToLong, SIZETToLong, ULongPtrToLong, ULongPtrToLong function [Windows Shell], _shell_ULongPtrToLong, intsafe/ULongPtrToLong, shell.ULongPtrToLong
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
 - ULongPtrToLong
 - intsafe/ULongPtrToLong
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
 - ULongPtrToLong
---

# ULongPtrToLong function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>LONG</b>.

## -parameters

### -param ulOperand [in]

Type: <b>ULONG_PTR</b>

The value to be converted.

### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SIZETToLong</b> is an alias for this function.

<b>DWordPtrToLong</b> is an alias for this function.

