---
UID: NS:directml.DML_ELEMENT_WISE_CEIL_OPERATOR_DESC
title: DML_ELEMENT_WISE_CEIL_OPERATOR_DESC
description: Describes a DirectML math operator that performs the element-wise ceiling function f(x) = ceil(x * scale + bias), where the scale and bias terms are optional. The ceiling of x is the smallest integer that is greater than or equal to x.
old-location: direct3d12\dml_element_wise_ceil_operator_desc.htm
tech.root: direct3d12
ms.assetid: AE327416-2165-4383-B301-176211E8BE65
ms.date: 12/5/2018
ms.keywords: DML_ELEMENT_WISE_CEIL_OPERATOR_DESC, DML_ELEMENT_WISE_CEIL_OPERATOR_DESC structure, direct3d12.dml_element_wise_ceil_operator_desc, directml/DML_ELEMENT_WISE_CEIL_OPERATOR_DESC
ms.topic: struct
f1_keywords:
- directml/DML_ELEMENT_WISE_CEIL_OPERATOR_DESC
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ELEMENT_WISE_CEIL_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ELEMENT_WISE_CEIL_OPERATOR_DESC structure


## -description






Describes a DirectML math operator that performs the element-wise ceiling function f(x) = ceil(x * scale + bias), where the scale and bias terms are optional. The ceiling of x is the smallest integer that is greater than or equal to x.

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

