---
UID: NF:intsafe.ULongPtrToLongLong
title: ULongPtrToLongLong function (intsafe.h)
description: Converts a value of type SIZE_T to a value of type INT64.
helpviewer_keywords: ["SIZETToInt64","SIZETToInt64 function [Windows Shell]","ULongPtrToLongLong","_shell_SIZETToInt64","intsafe/SIZETToInt64","shell.SIZETToInt64","shell.SIZETToInt64_1"]
old-location: shell\SIZETToInt64_1.htm
tech.root: shell
ms.assetid: fee8914c-8acb-41e9-b239-3844a4ef1289
ms.date: 12/05/2018
ms.keywords: SIZETToInt64, SIZETToInt64 function [Windows Shell], ULongPtrToLongLong, _shell_SIZETToInt64, intsafe/SIZETToInt64, shell.SIZETToInt64, shell.SIZETToInt64_1
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
 - ULongPtrToLongLong
 - intsafe/ULongPtrToLongLong
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
 - SIZETToInt64
---

# ULongPtrToLongLong function


## -description

Converts a value of type <b>SIZE_T</b> to a value of type <b>INT64</b>.

## -parameters

### -param ulOperand [in]

Type: <b>SIZE_T</b>

The value to be converted.

### -param pllResult [out]

Type: <b>INT64*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

