---
UID: NF:intsafe.LongToULongLong
title: LongToULongLong function (intsafe.h)
description: Converts a value of type LONG to a value of type ULONGLONG.
helpviewer_keywords: ["LongToULongLong","LongToULongLong function [Windows Shell]","_shell_LongToULongLong","intsafe/LongToULongLong","shell.LongToULongLong"]
old-location: shell\LongToULongLong.htm
tech.root: shell
ms.assetid: 6ad0e928-b09b-41d7-be5a-fea9219edf4b
ms.date: 12/05/2018
ms.keywords: LongToULongLong, LongToULongLong function [Windows Shell], _shell_LongToULongLong, intsafe/LongToULongLong, shell.LongToULongLong
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
 - LongToULongLong
 - intsafe/LongToULongLong
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
 - LongToULongLong
---

# LongToULongLong function


## -description

Converts a value of type <b>LONG</b> to a value of type <b>ULONGLONG</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.

### -param pullResult [out]

Type: <b>ULONGLONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

