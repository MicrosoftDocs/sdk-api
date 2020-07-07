---
UID: NS:directml.DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
title: DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
description: Describes a DirectML math operator that performs the function of adding every element in *ATensor* to its corresponding element in *BTensor*, with the option for fused activation.
tech.root: direct3d12
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
 - DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
f1_keywords:
 - directml/DML_ELEMENT_WISE_ADD1_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML math operator that performs the function of adding every element in *ATensor* to its corresponding element in *BTensor*, f(a, b) = a + b, with the option for fused activation.

This operator supports in-place execution, meaning the output tensor is permitted to alias one of the input tensors during binding.

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the *A* tensor to read from.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the *B* tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field FusedActivation

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

An optional pointer to a constant [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the fused activation layer.

## -remarks

## -see-also
