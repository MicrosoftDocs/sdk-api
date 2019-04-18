---
UID: NS:directml.DML_BATCH_NORMALIZATION_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML operator that performs a batch normalization function on the input, y = scale * (x - batchMean) / sqrt(batchVariance + epsilon) + bias.
old-location: direct3d12\dml_batch_normalization_operator_desc.htm
tech.root: direct3d12
ms.assetid: 6589B3EF-1DB9-4E52-B0D2-31C94A725F07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_BATCH_NORMALIZATION_OPERATOR_DESC, DML_BATCH_NORMALIZATION_OPERATOR_DESC structure, direct3d12.dml_batch_normalization_operator_desc, directml/DML_BATCH_NORMALIZATION_OPERATOR_DESC
ms.topic: struct
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
 - DML_BATCH_NORMALIZATION_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_BATCH_NORMALIZATION_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a batch normalization function on the input, y = scale * (x - batchMean) / sqrt(batchVariance + epsilon) + bias.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field MeanTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing batchMean.


### -field VarianceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the batchVariance.


### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the scale.


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field Spatial

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to specify that locations are spatial, otherwise <b>FALSE</b>.


### -field Epsilon

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The epsilon value to use to avoid division by zero.


### -field FusedActivation

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

An optional pointer to a constant [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the fused activation layer.

