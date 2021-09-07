---
UID: NF:intsafe.UIntPtrToInt
title: UIntPtrToInt function (intsafe.h)
description: Converts a value of type SIZE_T to a value of type INT.
helpviewer_keywords: ["SIZETToInt","SIZETToInt function [Windows Shell]","UIntPtrToInt","_shell_SIZETToInt","intsafe/SIZETToInt","shell.SIZETToInt","shell.SIZETToInt_1"]
old-location: shell\SIZETToInt_1.htm
tech.root: shell
ms.assetid: 00a1229b-28cf-4d8e-a59a-0c91872b2e06
ms.date: 12/05/2018
ms.keywords: SIZETToInt, SIZETToInt function [Windows Shell], UIntPtrToInt, _shell_SIZETToInt, intsafe/SIZETToInt, shell.SIZETToInt, shell.SIZETToInt_1
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
 - UIntPtrToInt
 - intsafe/UIntPtrToInt
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
 - SIZETToInt
---

# UIntPtrToInt function


## -description

Converts a value of type <b>SIZE_T</b> to a value of type <b>INT</b>.

## -parameters

### -param uOperand [in]

Type: <b>SIZE_T</b>

The value to be converted.

### -param piResult [out]

Type: <b>INT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

