---
UID: NF:intsafe.LongToUShort
title: LongToUShort function (intsafe.h)
description: Converts a value of type LONG to a value of type USHORT.
helpviewer_keywords: ["LongToUShort","LongToUShort function [Windows Shell]","LongToWord","_shell_LongToUShort","intsafe/LongToUShort","shell.LongToUShort"]
old-location: shell\LongToUShort.htm
tech.root: shell
ms.assetid: 45f9f7b0-a090-4162-8afc-ceaa85d3d848
ms.date: 12/05/2018
ms.keywords: LongToUShort, LongToUShort function [Windows Shell], LongToWord, _shell_LongToUShort, intsafe/LongToUShort, shell.LongToUShort
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
 - LongToUShort
 - intsafe/LongToUShort
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
 - LongToUShort
---

# LongToUShort function


## -description

Converts a value of type <b>LONG</b> to a value of type <b>USHORT</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.

### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongToWord</b> is an alias for this function.

