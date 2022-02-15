---
UID: NF:intsafe.UShortToShort
title: UShortToShort function (intsafe.h)
description: Converts a value of type USHORT to a value of type SHORT.
helpviewer_keywords: ["UShortToShort","UShortToShort function [Windows Shell]","WordToShort","_shell_UShortToShort","intsafe/UShortToShort","shell.UShortToShort"]
old-location: shell\UShortToShort.htm
tech.root: shell
ms.assetid: 77fd8f32-0b24-4d03-8a6e-d7512c8c6482
ms.date: 12/05/2018
ms.keywords: UShortToShort, UShortToShort function [Windows Shell], WordToShort, _shell_UShortToShort, intsafe/UShortToShort, shell.UShortToShort
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
 - UShortToShort
 - intsafe/UShortToShort
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
 - UShortToShort
---

# UShortToShort function


## -description

Converts a value of type <b>USHORT</b> to a value of type <b>SHORT</b>.

## -parameters

### -param usOperand [in]

Type: <b>USHORT</b>

The value to be converted.

### -param psResult [out]

Type: <b>SHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>WordToShort</b> is an alias for this function.

