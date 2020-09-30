---
UID: NF:intsafe.ULongToIntPtr
title: ULongToIntPtr function (intsafe.h)
description: Converts a value of type ULONG to a value of type INT_PTR.
helpviewer_keywords: ["DWordToIntPtr","DWordToPtrdiffT","ULongToIntPtr","ULongToIntPtr function [Windows Shell]","ULongToPtrdiffT","_shell_ULongToIntPtr","intsafe/ULongToIntPtr","shell.ULongToIntPtr"]
old-location: shell\ULongToIntPtr.htm
tech.root: shell
ms.assetid: 0d7cd4f0-03fd-43a2-b3e9-10441f65bf78
ms.date: 12/05/2018
ms.keywords: DWordToIntPtr, DWordToPtrdiffT, ULongToIntPtr, ULongToIntPtr function [Windows Shell], ULongToPtrdiffT, _shell_ULongToIntPtr, intsafe/ULongToIntPtr, shell.ULongToIntPtr
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
 - ULongToIntPtr
 - intsafe/ULongToIntPtr
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
 - ULongToIntPtr
---

# ULongToIntPtr function


## -description

Converts a value of type <b>ULONG</b> to a value of type <b>INT_PTR</b>.

## -parameters

### -param ulOperand [in]

Type: <b>ULONG</b>

The value to be converted.

### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordToPtrdiffT</b> is an alias for this function.

<b>ULongToPtrdiffT</b> is an alias for this function.

<b>DWordToIntPtr</b> is an alias for this function.

