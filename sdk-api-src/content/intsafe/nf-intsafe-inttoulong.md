---
UID: NF:intsafe.IntToULong
title: IntToULong function (intsafe.h)
description: Converts a value of type INT to a value of type ULONG.
helpviewer_keywords: ["IntToDWord","IntToULong","IntToULong function [Windows Shell]","_shell_IntToULong","intsafe/IntToULong","shell.IntToULong"]
old-location: shell\IntToULong.htm
tech.root: shell
ms.assetid: 060915cf-d7a2-48ef-b2b6-303f2cc86c94
ms.date: 12/05/2018
ms.keywords: IntToDWord, IntToULong, IntToULong function [Windows Shell], _shell_IntToULong, intsafe/IntToULong, shell.IntToULong
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
 - IntToULong
 - intsafe/IntToULong
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
 - IntToULong
---

# IntToULong function


## -description

Converts a value of type <b>INT</b> to a value of type <b>ULONG</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>IntToDWord</b> is an alias for this function.

