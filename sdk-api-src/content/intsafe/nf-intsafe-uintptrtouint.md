---
UID: NF:intsafe.UIntPtrToUInt
title: UIntPtrToUInt function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type UINT.
helpviewer_keywords: ["SizeTToUInt","UIntPtrToUInt","UIntPtrToUInt function [Windows Shell]","_shell_UIntPtrToUInt","intsafe/UIntPtrToUInt","shell.UIntPtrToUInt"]
old-location: shell\UIntPtrToUInt.htm
tech.root: shell
ms.assetid: 298333ae-1efc-41b8-a8e6-83c2c0d4088e
ms.date: 12/05/2018
ms.keywords: SizeTToUInt, UIntPtrToUInt, UIntPtrToUInt function [Windows Shell], _shell_UIntPtrToUInt, intsafe/UIntPtrToUInt, shell.UIntPtrToUInt
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
 - UIntPtrToUInt
 - intsafe/UIntPtrToUInt
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
 - UIntPtrToUInt
---

# UIntPtrToUInt function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>UINT</b>.

## -parameters

### -param uOperand [in]

Type: <b>UINT_PTR</b>

The value to be converted.

### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SizeTToUInt</b> is an alias for this function.

