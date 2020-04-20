---
UID: NS:directml.DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC
title: DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC
description: Describes a DirectML operator that performs a log-of-softmax activation function on the input, f(x_i) = log(exp(x_i - max(X)) / sum(exp(X - max(X)))) = (x_i - max(X)) - log(sum(exp(x - max(X)))).helpviewer_keywords: ["DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC","DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC structure","direct3d12.dml_activation_log_softmax_operator_desc","directml/DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC"]
old-location: direct3d12\dml_activation_log_softmax_operator_desc.htm
tech.root: direct3d12
ms.assetid: 6CC6B311-A2D7-4701-9393-57D5838EF7A4
ms.date: 12/5/2018
ms.keywords: DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC, DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC structure, direct3d12.dml_activation_log_softmax_operator_desc, directml/DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC
f1_keywords:
- directml/DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC
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
- DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ACTIVATION_LOG_SOFTMAX_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a log-of-softmax activation function on the input, f(x_i) = log(exp(x_i - max(X)) / sum(exp(X - max(X))))
 = (x_i - max(X)) - log(sum(exp(x - max(X)))).


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


## -see-also




[DML_ACTIVATION_SOFTMAX_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_activation_softmax_operator_desc)
 

 

