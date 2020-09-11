---
UID: NS:directml.DML_ELEMENT_WISE_SINH_OPERATOR_DESC
title: DML_ELEMENT_WISE_SINH_OPERATOR_DESC
description: Describes a DirectML trigonometric operator that performs the element-wise hyperbolic sine function f(x) = ((e^x - e^-x) / 2) * scale + bias, where the scale and bias terms are optional.
tech.root: directml
ms.date: 01/30/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directml.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_ELEMENT_WISE_SINH_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_SINH_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_SINH_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML trigonometric operator that performs the element-wise hyperbolic sine function f(x) = ((e^x - e^-x) / 2) * scale + bias, where the scale and bias terms are optional.

This operator supports in-place execution, meaning the output tensor is permitted to alias the input tensor during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field ScaleBias

Type: **const [DML_SCALE_BIAS](/windows/desktop/api/directml/ns-directml-dml_scale_bias)\***

An optional pointer to a constant [DML_SCALE_BIAS](/windows/desktop/api/directml/ns-directml-dml_scale_bias) containing scale and bias to apply to the input. If present, this has the effect of applying the function g(x) = x * scale + bias to each element before this topic's operator is applied.

## -remarks

## -see-also

