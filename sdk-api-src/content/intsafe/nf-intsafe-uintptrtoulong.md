---
UID: NF:intsafe.UIntPtrToULong
title: UIntPtrToULong function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type ULONG.
helpviewer_keywords: ["SizeTToDWord","SizeTToULong","UIntPtrToDWord","UIntPtrToULong","UIntPtrToULong function [Windows Shell]","_shell_UIntPtrToULong","intsafe/UIntPtrToULong","shell.UIntPtrToULong"]
old-location: shell\UIntPtrToULong.htm
tech.root: shell
ms.assetid: 29d33dd1-c6fd-445b-a340-0a194735a763
ms.date: 12/05/2018
ms.keywords: SizeTToDWord, SizeTToULong, UIntPtrToDWord, UIntPtrToULong, UIntPtrToULong function [Windows Shell], _shell_UIntPtrToULong, intsafe/UIntPtrToULong, shell.UIntPtrToULong
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
 - UIntPtrToULong
 - intsafe/UIntPtrToULong
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
 - UIntPtrToULong
---

# UIntPtrToULong function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>ULONG</b>.

## -parameters

### -param uOperand [in]

Type: <b>UINT_PTR</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SizeTToULong</b> is an alias for this function.

<b>SizeTToDWord</b> is an alias for this function.

<b>UIntPtrToDWord</b> is an alias for this function.

