---
UID: NF:intsafe.ULongLongToLong
title: ULongLongToLong function (intsafe.h)
description: Converts a value of type ULONGLONG to a value of type LONG.
helpviewer_keywords: ["ULongLongToLong","ULongLongToLong function [Windows Shell]","_shell_ULongLongToLong","intsafe/ULongLongToLong","shell.ULongLongToLong"]
old-location: shell\ULongLongToLong.htm
tech.root: shell
ms.assetid: 19721f40-e347-49d4-a296-46131229c2d0
ms.date: 12/05/2018
ms.keywords: ULongLongToLong, ULongLongToLong function [Windows Shell], _shell_ULongLongToLong, intsafe/ULongLongToLong, shell.ULongLongToLong
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
 - ULongLongToLong
 - intsafe/ULongLongToLong
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
 - ULongLongToLong
---

# ULongLongToLong function


## -description

Converts a value of type <b>ULONGLONG</b> to a value of type <b>LONG</b>.

## -parameters

### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.

### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

