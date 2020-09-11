---
UID: NS:directml.DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
title: DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
description: Describes a DirectML operator that performs the element-wise constant power function f(x) = pow(x * scale + bias, exponent), where the scale and bias terms are optional. The power function raises every element in the input to the power of the exponent.
helpviewer_keywords: ["DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC","DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC structure","direct3d12.dml_element_wise_constant_pow_operator_desc","directml/DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_constant_pow_operator_desc.htm
tech.root: directml
ms.assetid: A9E4FD02-7819-4805-91B1-80E82CF94B6B
ms.date: 12/5/2018
ms.keywords: DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC, DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC structure, direct3d12.dml_element_wise_constant_pow_operator_desc, directml/DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC
---

# DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC structure


## -description

Describes a DirectML operator that performs the element-wise constant power function f(x) = pow(x * scale + bias, exponent), where the scale and bias terms are optional. The power function raises every element in the input to the power of the exponent.

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

### -field Exponent

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The exponent to which to raise the input.

## -see-also

[DML_ELEMENT_WISE_POW_OPERATOR_DESC<](/windows/desktop/api/directml/ns-directml-dml_element_wise_pow_operator_desc)

