---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
description: Describes a DirectML operator that performs a mean variance normalization function on the input tensor.
helpviewer_keywords: ["DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC","DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_mean_variance_normalization_operator_desc","directml/DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_mean_variance_normalization_operator_desc.htm
tech.root: directml
ms.assetid: AF70005F-BDBB-45C9-9066-70A574D5BC0E
ms.date: 12/5/2018
ms.keywords: DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC, DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC structure, direct3d12.dml_mean_variance_normalization_operator_desc, directml/DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
f1_keywords:
- directml/DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a mean variance normalization function on the input tensor.

Exponent = Const(2.0)

Epsilon = Const(1e-9)

X_RM = ReduceMean(X)

EX_squared = Pow(X_RM, Exponent)

X_squared = Pow(X, Exponent)

E_Xsquared = ReduceMean(X_squared)

Variance = Sub(E_Xsquared, EX_squared)

STD = Sqrt(Variance)

X_variance = Sub(X, X_RM)

Processed_STD = Add(STD, Epsilon)

X_MVN = Div(X_variance, Processed_STD)


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the scale.


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field CrossChannel

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the LRN layer is channel-wise (cross-channel). Otherwise, <b>FALSE</b>.


### -field NormalizeVariance

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the variance should be normalized. Otherwise, <b>FALSE</b>.


### -field Epsilon

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero.


### -field FusedActivation

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

An optional pointer to a constant [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the fused activation layer.

