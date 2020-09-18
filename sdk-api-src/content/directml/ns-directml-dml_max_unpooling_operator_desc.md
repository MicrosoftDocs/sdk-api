---
UID: NS:directml.DML_MAX_UNPOOLING_OPERATOR_DESC
title: DML_MAX_UNPOOLING_OPERATOR_DESC
description: Describes a DirectML operator that fills the output tensor of the given shape (either explicit, or the input shape plus padding) with zeros, then writes each value from the input tensor into the output tensor at the element offset from the corresponding indices array.
tech.root: directml
ms.date: 01/31/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - DML_MAX_UNPOOLING_OPERATOR_DESC
f1_keywords:
 - DML_MAX_UNPOOLING_OPERATOR_DESC
 - directml/DML_MAX_UNPOOLING_OPERATOR_DESC
---

## -description

Describes a DirectML operator that fills the output tensor of the given shape (either explicit, or the input shape plus padding) with zeros, then writes each value from the input tensor into the output tensor at the element offset from the corresponding indices array.

**DML_MAX_UNPOOLING_OPERATOR_DESC** is the inverse of [DML_MAX_POOLING_OPERATOR_DESC](./ns-directml-dml_max_pooling_operator_desc.md).

All indices should be unique, and within bounds. The value written for duplicate indices is not defined; out-of-bounds indices yield no write.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the indices.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.