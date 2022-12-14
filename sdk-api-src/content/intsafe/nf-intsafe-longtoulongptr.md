---
UID: NF:intsafe.LongToULongPtr
title: LongToULongPtr function (intsafe.h)
description: Converts a value of type LONG to a value of type ULONG_PTR.
helpviewer_keywords: ["LongToDWordPtr","LongToSIZET","LongToULongPtr","LongToULongPtr function [Windows Shell]","PtrdiffTToDWordPtr","_shell_LongToULongPtr","intsafe/LongToULongPtr","shell.LongToULongPtr"]
old-location: shell\LongToULongPtr.htm
tech.root: shell
ms.assetid: fe2669b2-6121-4348-ac7b-f89a0121b994
ms.date: 12/05/2018
ms.keywords: LongToDWordPtr, LongToSIZET, LongToULongPtr, LongToULongPtr function [Windows Shell], PtrdiffTToDWordPtr, _shell_LongToULongPtr, intsafe/LongToULongPtr, shell.LongToULongPtr
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
 - LongToULongPtr
 - intsafe/LongToULongPtr
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
 - LongToULongPtr
---

# LongToULongPtr function


## -description

Converts a value of type <b>LONG</b> to a value of type <b>ULONG_PTR</b>.

## -parameters

### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongToSIZET</b> is an alias for this function.

<b>LongToDWordPtr</b> is an alias for this function.

<b>PtrdiffTToDWordPtr</b> is an alias for this function.

