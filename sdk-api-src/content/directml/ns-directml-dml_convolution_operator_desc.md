---
UID: NS:directml.DML_CONVOLUTION_OPERATOR_DESC
title: DML_CONVOLUTION_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML matrix multiplication operator that performs a convolution function on the input, out[j] = x[i]*w[0] + x[i+1]*w[1] + x[i+2]*w[2] + ... + x[i+k]*w[k] + bias.
old-location: direct3d12\dml_convolution_operator_desc.htm
tech.root: direct3d12
ms.assetid: F504A454-2D0B-472D-BB45-EE5690A1160C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_CONVOLUTION_OPERATOR_DESC, DML_CONVOLUTION_OPERATOR_DESC structure, direct3d12.dml_convolution_operator_desc, directml/DML_CONVOLUTION_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_CONVOLUTION_OPERATOR_DESC"
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
 - DML_CONVOLUTION_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_CONVOLUTION_OPERATOR_DESC structure


## -description






Describes a DirectML matrix multiplication operator that performs a convolution function on the input, out[j] = x[i]*w[0] + x[i+1]*w[1] + x[i+2]*w[2] + ... + x[i+k]*w[k] + bias.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field FilterTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the filter.


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field Mode

Type: [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode)

The mode to use for the convolution operation. If in doubt, use <b>DML_CONVOLUTION_MODE_CROSS_CORRELATION</b>—it is appropriate for the vast majority of machine learning (ML) models.


### -field Direction

Type: [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction)

The direction of the convolution operation.


### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of dimensions. This field determines the size of the <i>Strides</i>,  <i>Dilations</i>, <i>StartPadding</i>, <i>EndPadding</i>, and <i>OutputPadding</i> arrays.


### -field Strides

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the lengths of the strides of the tensor.


### -field Dilations

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the value of the  dilation along each axis of the filter.


### -field StartPadding

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the padding (number of pixels added) to the start of the corresponding axis. Padding defaults to 0 along the start and end of each axis.


### -field EndPadding

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the padding (number of pixels added) to the end of the corresponding axis. Padding defaults to 0 along the start and end of each axis.


### -field OutputPadding

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the padding (number of pixels added) to the output for the corresponding axis. Padding defaults to 0.


### -field GroupCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of groups.


### -field FusedActivation

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

An optional pointer to a constant [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the fused activation layer.

