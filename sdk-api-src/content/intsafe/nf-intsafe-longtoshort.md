---
UID: NF:intsafe.LongToShort
title: LongToShort function (intsafe.h)
description: Converts a value of type LONG to a value of type SHORT.
helpviewer_keywords: ["LongToShort","LongToShort function [Windows Shell]","_shell_LongToShort","intsafe/LongToShort","shell.LongToShort"]
old-location: shell\LongToShort.htm
tech.root: shell
ms.assetid: 7396ee67-c8bd-45e5-8500-ae5101e659d5
ms.date: 12/05/2018
ms.keywords: LongToShort, LongToShort function [Windows Shell], _shell_LongToShort, intsafe/LongToShort, shell.LongToShort
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
 - LongToShort
 - intsafe/LongToShort
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
 - LongToShort
---

# LongToShort function


## -description

Converts a value of type <b>LONG</b> to a value of type <b>SHORT</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.

### -param psResult [out]

Type: <b>SHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

