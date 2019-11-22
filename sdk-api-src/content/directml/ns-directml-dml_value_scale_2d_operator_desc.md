---
UID: NS:directml.DML_VALUE_SCALE_2D_OPERATOR_DESC
title: DML_VALUE_SCALE_2D_OPERATOR_DESC

description: Describes a DirectML operator that performs an element-wise scale-and-bias function on the values in the input tensor.
old-location: direct3d12\dml_value_scale_2d_operator_desc.htm
tech.root: direct3d12
ms.assetid: 205124C7-9296-4D13-9EC9-55B03D4E0595

ms.date: 12/5/2018
ms.keywords: DML_VALUE_SCALE_2D_OPERATOR_DESC, DML_VALUE_SCALE_2D_OPERATOR_DESC structure, direct3d12.dml_value_scale_2d_operator_desc, directml/DML_VALUE_SCALE_2D_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_VALUE_SCALE_2D_OPERATOR_DESC"
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
 - DML_VALUE_SCALE_2D_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_VALUE_SCALE_2D_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs an element-wise scale-and-bias function on the values in the input tensor. This operator is similar to using an **ELEMENT_WISE_IDENTITY** operator with a scale and bias, except that **VALUE_SCALE_2D** applies a different bias for each channel rather than a single bias for the entire tensor.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field Scale

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The scale to apply. You can use a default value of 1.0.


### -field ChannelCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>Bias</i> array. This field must be set to either 1 or 3, and must also match the size of the C dimension of the input tensor.


### -field Bias

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a>*</b>

A pointer to a constant array of <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a> containing the bias term for each dimension of the input tensor.

