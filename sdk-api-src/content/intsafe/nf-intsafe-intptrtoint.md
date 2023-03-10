---
UID: NF:intsafe.IntPtrToInt
title: IntPtrToInt function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type INT.
helpviewer_keywords: ["IntPtrToInt","IntPtrToInt function [Windows Shell]","PtrdiffTToInt","_shell_IntPtrToInt","intsafe/IntPtrToInt","shell.IntPtrToInt"]
old-location: shell\IntPtrToInt.htm
tech.root: shell
ms.assetid: a2ea1196-b503-4845-904a-26bc334b5275
ms.date: 12/05/2018
ms.keywords: IntPtrToInt, IntPtrToInt function [Windows Shell], PtrdiffTToInt, _shell_IntPtrToInt, intsafe/IntPtrToInt, shell.IntPtrToInt
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
 - IntPtrToInt
 - intsafe/IntPtrToInt
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
 - IntPtrToInt
---

# IntPtrToInt function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>INT</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT_PTR</b>

The value to convert.

### -param piResult [out]

Type: <b>INT*</b>

The converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>PtrdiffTToInt</b> is an alias for this function.

