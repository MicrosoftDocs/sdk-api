---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML math operator that performs the element-wise clip function f(x) = clamp(x * scale + bias, minValue, maxValue), where the scale and bias terms are optional, and where clamp(x) = min(maxValue, max(minValue, x)).
old-location: direct3d12\dml_element_wise_clip_operator_desc.htm
tech.root: direct3d12
ms.assetid: 980CC8B8-A0D8-40BB-8506-ECB8F9EFAB11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_ELEMENT_WISE_CLIP_OPERATOR_DESC, DML_ELEMENT_WISE_CLIP_OPERATOR_DESC structure, direct3d12.dml_element_wise_clip_operator_desc, directml/DML_ELEMENT_WISE_CLIP_OPERATOR_DESC
ms.topic: struct
f1_keywords: ["directml/DML_ELEMENT_WISE_CLIP_OPERATOR_DESC"]
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
 - DML_ELEMENT_WISE_CLIP_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ELEMENT_WISE_CLIP_OPERATOR_DESC structure


## -description






Describes a DirectML math operator that performs the element-wise clip function f(x) = clamp(x * scale + bias, minValue, maxValue), where the scale and bias terms are optional, and where clamp(x) = min(maxValue, max(minValue, x)). This operator clamps (or limits) every element in the input within the closed interval [min, max].


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


### -field Min

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The minimum value, below which the operator replaces the value with <i>Min</i>. This is referred to as minValue in the operator description above in order not to confuse it with the min function.


### -field Max

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The maximum value, above which the operator replaces the value with <i>Max</i>. This is referred to as maxValue in the operator description above in order not to confuse it with the max function.

