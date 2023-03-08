---
UID: NF:intsafe.LongPtrToULongPtr
title: LongPtrToULongPtr function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type ULONG_PTR.
helpviewer_keywords: ["LongPtrToDWordPtr","LongPtrToSIZET","LongPtrToULongPtr","LongPtrToULongPtr function [Windows Shell]","SSIZETToDWordPtr","SSIZETToSIZET","SSIZETToULongPtr","_shell_LongPtrToULongPtr","intsafe/LongPtrToULongPtr","shell.LongPtrToULongPtr"]
old-location: shell\LongPtrToULongPtr.htm
tech.root: shell
ms.assetid: c289c4cd-abb7-4483-b0a7-6eacadefeedc
ms.date: 12/05/2018
ms.keywords: LongPtrToDWordPtr, LongPtrToSIZET, LongPtrToULongPtr, LongPtrToULongPtr function [Windows Shell], SSIZETToDWordPtr, SSIZETToSIZET, SSIZETToULongPtr, _shell_LongPtrToULongPtr, intsafe/LongPtrToULongPtr, shell.LongPtrToULongPtr
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
 - LongPtrToULongPtr
 - intsafe/LongPtrToULongPtr
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
 - LongPtrToULongPtr
---

# LongPtrToULongPtr function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>ULONG_PTR</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG_PTR</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongPtrToSIZET</b> is an alias for this function.

<b>SSIZETToULongPtr</b> is an alias for this function.

<b>SSIZETToSIZET</b> is an alias for this function.

<b>SSIZETToDWordPtr</b> is an alias for this function.

<b>LongPtrToDWordPtr</b> is an alias for this function.

