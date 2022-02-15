---
UID: NF:intsafe.ULongPtrToLongPtr
title: ULongPtrToLongPtr function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type LONG_PTR.
helpviewer_keywords: ["DWordPtrToLongPtr","DWordPtrToSSIZET","SIZETToLongPtr","SIZETToSSIZET","ULongPtrToLongPtr","ULongPtrToLongPtr function [Windows Shell]","ULongPtrToSSIZET","_shell_ULongPtrToLongPtr","intsafe/ULongPtrToLongPtr","shell.ULongPtrToLongPtr"]
old-location: shell\ULongPtrToLongPtr.htm
tech.root: shell
ms.assetid: 0da89cb7-721c-47d4-8f33-c8f44eb996b1
ms.date: 12/05/2018
ms.keywords: DWordPtrToLongPtr, DWordPtrToSSIZET, SIZETToLongPtr, SIZETToSSIZET, ULongPtrToLongPtr, ULongPtrToLongPtr function [Windows Shell], ULongPtrToSSIZET, _shell_ULongPtrToLongPtr, intsafe/ULongPtrToLongPtr, shell.ULongPtrToLongPtr
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
 - ULongPtrToLongPtr
 - intsafe/ULongPtrToLongPtr
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
 - ULongPtrToLongPtr
---

# ULongPtrToLongPtr function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>LONG_PTR</b>.

## -parameters

### -param ulOperand [in]

Type: <b>ULONG_PTR</b>

The value to be converted.

### -param plResult [out]

Type: <b>LONG_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordPtrToSSIZET</b> is an alias for this function.

<b>ULongPtrToSSIZET</b> is an alias for this function.

<b>SIZETToSSIZET</b> is an alias for this function.

<b>SIZETToLongPtr</b> is an alias for this function.

<b>DWordPtrToLongPtr</b> is an alias for this function.

