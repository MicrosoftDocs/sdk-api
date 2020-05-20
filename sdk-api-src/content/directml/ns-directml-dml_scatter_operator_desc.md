---
UID: NS:directml.DML_SCATTER_OPERATOR_DESC
title: DML_SCATTER_OPERATOR_DESC
description: Describes a DirectML operator that copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.
tech.root: direct3d12
ms.date: 01/31/2020
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
 - DML_SCATTER_OPERATOR_DESC
f1_keywords:
 - directml/DML_SCATTER_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Describes a DirectML operator that copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.

**DML_SCATTER_OPERATOR_DESC** is the inverse of [DML_GATHER_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_operator_desc).

If two output element indices overlap (which is invalid), then only the last write takes effect.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the indices.

### -field UpdatesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the updates.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis dimension to add to *OutputTensor*.

## -remarks

## -see-also
