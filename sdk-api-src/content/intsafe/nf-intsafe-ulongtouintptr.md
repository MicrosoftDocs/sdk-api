---
UID: NF:intsafe.ULongToUIntPtr
title: ULongToUIntPtr function (intsafe.h)
description: Converts a value of type ULONG to a value of type UINT_PTR.
helpviewer_keywords: ["DWordToUIntPtr","ULongToUIntPtr","ULongToUIntPtr function [Windows Shell]","_shell_ULongToUIntPtr","intsafe/ULongToUIntPtr","shell.ULongToUIntPtr"]
old-location: shell\ULongToUIntPtr.htm
tech.root: shell
ms.assetid: 36431909-7456-459f-84f7-7ec101cebb98
ms.date: 12/05/2018
ms.keywords: DWordToUIntPtr, ULongToUIntPtr, ULongToUIntPtr function [Windows Shell], _shell_ULongToUIntPtr, intsafe/ULongToUIntPtr, shell.ULongToUIntPtr
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
 - ULongToUIntPtr
 - intsafe/ULongToUIntPtr
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
 - ULongToUIntPtr
---

# ULongToUIntPtr function


## -description

Converts a value of type <b>ULONG</b> to a value of type <b>UINT_PTR</b>.

## -parameters

### -param ulOperand [in]

Type: <b>ULONG</b>

The value to be converted.

### -param puiResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordToUIntPtr</b> is an alias for this function.

