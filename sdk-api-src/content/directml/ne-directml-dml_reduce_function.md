---
UID: NE:directml.DML_REDUCE_FUNCTION
title: DML_REDUCE_FUNCTION
description: Defines constants that specify the specific reduction algorithm to use for the DirectML reduce operator (as described by the DML_REDUCE_OPERATOR_DESC structure).
helpviewer_keywords: ["DML_REDUCE_FUNCTION","DML_REDUCE_FUNCTION enumeration","DML_REDUCE_FUNCTION_ARGMAX","DML_REDUCE_FUNCTION_ARGMIN","DML_REDUCE_FUNCTION_AVERAGE","DML_REDUCE_FUNCTION_L1","DML_REDUCE_FUNCTION_L2","DML_REDUCE_FUNCTION_LOG_SUM","DML_REDUCE_FUNCTION_LOG_SUM_EXP","DML_REDUCE_FUNCTION_MAX","DML_REDUCE_FUNCTION_MIN","DML_REDUCE_FUNCTION_MULTIPLY","DML_REDUCE_FUNCTION_SUM","DML_REDUCE_FUNCTION_SUM_SQUARE","direct3d12.dml_reduce_function","directml/DML_REDUCE_FUNCTION","directml/DML_REDUCE_FUNCTION_ARGMAX","directml/DML_REDUCE_FUNCTION_ARGMIN","directml/DML_REDUCE_FUNCTION_AVERAGE","directml/DML_REDUCE_FUNCTION_L1","directml/DML_REDUCE_FUNCTION_L2","directml/DML_REDUCE_FUNCTION_LOG_SUM","directml/DML_REDUCE_FUNCTION_LOG_SUM_EXP","directml/DML_REDUCE_FUNCTION_MAX","directml/DML_REDUCE_FUNCTION_MIN","directml/DML_REDUCE_FUNCTION_MULTIPLY","directml/DML_REDUCE_FUNCTION_SUM","directml/DML_REDUCE_FUNCTION_SUM_SQUARE"]
old-location: direct3d12\dml_reduce_function.htm
tech.root: directml
ms.assetid: 538BAB2E-C7AE-4A9E-AD87-4BDEEB677504
ms.date: 12/5/2018
ms.keywords: DML_REDUCE_FUNCTION, DML_REDUCE_FUNCTION enumeration, DML_REDUCE_FUNCTION_ARGMAX, DML_REDUCE_FUNCTION_ARGMIN, DML_REDUCE_FUNCTION_AVERAGE, DML_REDUCE_FUNCTION_L1, DML_REDUCE_FUNCTION_L2, DML_REDUCE_FUNCTION_LOG_SUM, DML_REDUCE_FUNCTION_LOG_SUM_EXP, DML_REDUCE_FUNCTION_MAX, DML_REDUCE_FUNCTION_MIN, DML_REDUCE_FUNCTION_MULTIPLY, DML_REDUCE_FUNCTION_SUM, DML_REDUCE_FUNCTION_SUM_SQUARE, direct3d12.dml_reduce_function, directml/DML_REDUCE_FUNCTION, directml/DML_REDUCE_FUNCTION_ARGMAX, directml/DML_REDUCE_FUNCTION_ARGMIN, directml/DML_REDUCE_FUNCTION_AVERAGE, directml/DML_REDUCE_FUNCTION_L1, directml/DML_REDUCE_FUNCTION_L2, directml/DML_REDUCE_FUNCTION_LOG_SUM, directml/DML_REDUCE_FUNCTION_LOG_SUM_EXP, directml/DML_REDUCE_FUNCTION_MAX, directml/DML_REDUCE_FUNCTION_MIN, directml/DML_REDUCE_FUNCTION_MULTIPLY, directml/DML_REDUCE_FUNCTION_SUM, directml/DML_REDUCE_FUNCTION_SUM_SQUARE
req.header: directml.h
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
 - DML_REDUCE_FUNCTION
 - directml/DML_REDUCE_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_REDUCE_FUNCTION
---

## -description

Defines constants that specify the specific reduction algorithm to use for the DirectML reduce operator (as described by the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) structure).

## -enum-fields

### -field DML_REDUCE_FUNCTION_ARGMAX

Indicates a reduction function that computes the indices of the max elements of the input tensor's elements along the specified axis, int32 {i j k ..} = maxindex(X Y Z …).

### -field DML_REDUCE_FUNCTION_ARGMIN

Indicates a reduction function that computes the indices of the min elements of the input tensor's elements along the specified axis, int32 {i j k ..} = minindex(X Y Z …).

### -field DML_REDUCE_FUNCTION_AVERAGE

Indicates a reduction function that computes the mean of the input tensor's elements along the specified axes, x = (x1 + x2 + ... + xn) / n.

### -field DML_REDUCE_FUNCTION_L1

Indicates a reduction function that computes the L1 norm of the input tensor's elements along the specified axes, x = \|x1\| + \|x2\| + ... + \|xn\|.

### -field DML_REDUCE_FUNCTION_L2

Indicates a reduction function that computes the L2 norm of the input tensor's elements along the specified axes, x = sqrt(x1^2 + x2^2 + ... + xn^2).

### -field DML_REDUCE_FUNCTION_LOG_SUM

Indicates a reduction function that computes the log sum of the input tensor's elements along the specified axes, x = log(x1 + x2 + ... + xn).

### -field DML_REDUCE_FUNCTION_LOG_SUM_EXP

Indicates a reduction function that computes the log sum exponent of the input tensor's elements along the specified axes, x = log(exp(x1) + exp(x2) + ... + exp(xn)).

### -field DML_REDUCE_FUNCTION_MAX

Indicates a reduction function that computes the max of the input tensor's elements along the specified axes, x = max(max(max(x1, x2), x3), ..., xn).

### -field DML_REDUCE_FUNCTION_MIN

Indicates a reduction function that computes the min of the input tensor's elements along the specified axes, x = min(min(min(x1, x2), x3), ..., xn).

### -field DML_REDUCE_FUNCTION_MULTIPLY

Indicates a reduction function that computes the product of the input tensor's elements along the specified axes, x = (x1 * x2 * ... * xn).

### -field DML_REDUCE_FUNCTION_SUM

Indicates a reduction function that computes the sum  of the input tensor's elements along the specified axes, x = (x1 + x2 + ... + xn).

### -field DML_REDUCE_FUNCTION_SUM_SQUARE

Indicates a reduction function that computes the sum square of the input tensor's elements along the specified axes, x = x1^2 + x2^2 + ... + xn^2.

## -see-also

* [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc)
