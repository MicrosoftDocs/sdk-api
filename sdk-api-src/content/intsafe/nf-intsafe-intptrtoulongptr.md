---
UID: NF:intsafe.IntPtrToULongPtr
title: IntPtrToULongPtr function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type ULONG_PTR.
helpviewer_keywords: ["IntPtrToDWordPtr","IntPtrToSIZET","IntPtrToULongPtr","IntPtrToULongPtr function [Windows Shell]","PtrdiffTToSIZET","PtrdiffTToULongPtr","_shell_IntPtrToULongPtr","intsafe/IntPtrToULongPtr","shell.IntPtrToULongPtr"]
old-location: shell\IntPtrToULongPtr.htm
tech.root: shell
ms.assetid: 782cf560-20a6-40fd-877b-2326a286c392
ms.date: 12/05/2018
ms.keywords: IntPtrToDWordPtr, IntPtrToSIZET, IntPtrToULongPtr, IntPtrToULongPtr function [Windows Shell], PtrdiffTToSIZET, PtrdiffTToULongPtr, _shell_IntPtrToULongPtr, intsafe/IntPtrToULongPtr, shell.IntPtrToULongPtr
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
 - IntPtrToULongPtr
 - intsafe/IntPtrToULongPtr
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
 - IntPtrToULongPtr
---

# IntPtrToULongPtr function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>ULONG_PTR</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT_PTR</b>

The value to be converted.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>IntPtrToSIZET</b> is an alias for this function.

<b>PtrdiffTToULongPtr</b> is an alias for this function.

<b>PtrdiffTToSIZET</b> is an alias for this function.

<b>IntPtrToDWordPtr</b> is an alias for this function.

