---
UID: NF:intsafe.UIntToIntPtr
title: UIntToIntPtr function (intsafe.h)
description: Converts a value of type UINT to a value of type INT_PTR.
helpviewer_keywords: ["UIntToIntPtr","UIntToIntPtr function [Windows Shell]","UIntToPtrdiffT","_shell_UIntToIntPtr","intsafe/UIntToIntPtr","shell.UIntToIntPtr"]
old-location: shell\UIntToIntPtr.htm
tech.root: shell
ms.assetid: 055213c7-a412-4c44-bb21-4d4914cd97c8
ms.date: 12/05/2018
ms.keywords: UIntToIntPtr, UIntToIntPtr function [Windows Shell], UIntToPtrdiffT, _shell_UIntToIntPtr, intsafe/UIntToIntPtr, shell.UIntToIntPtr
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
 - UIntToIntPtr
 - intsafe/UIntToIntPtr
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
 - UIntToIntPtr
---

# UIntToIntPtr function


## -description

Converts a value of type <b>UINT</b> to a value of type <b>INT_PTR</b>.

## -parameters

### -param uOperand [in]

Type: <b>UINT</b>

The value to be converted.

### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>UIntToPtrdiffT</b> is an alias for this function.

