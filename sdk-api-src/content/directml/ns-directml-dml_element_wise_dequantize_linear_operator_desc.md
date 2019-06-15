---
UID: NS:directml.DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
title: DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML operator that performs the linear dequantize function on every element in InputTensor with respect to its corresponding element in ScaleTensor and ZeroPointTensor, f(input, scale, zero_point) = (input - zero_point) * scale.
old-location: direct3d12\dml_element_wise_dequantize_linear_operator_desc.htm
tech.root: direct3d12
ms.assetid: 474CB378-3EFC-414F-B75F-D41577D0787D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC, DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC structure, direct3d12.dml_element_wise_dequantize_linear_operator_desc, directml/DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
ms.topic: struct
f1_keywords: ["directml/DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC"]
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
 - DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs the linear dequantize function on every element in <i>InputTensor</i> with respect to its corresponding element in <i>ScaleTensor</i> and <i>ZeroPointTensor</i>, f(input, scale, zero_point)
= (input - zero_point) * scale. Quantizing involves converting to a lower-precision data type in order to accelerate arithmetic.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing scale.


### -field ZeroPointTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the zero point.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


## -see-also




[DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_element_wise_quantize_linear_operator_desc)
 

 

