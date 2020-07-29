---
UID: NS:directml.DML_ONE_HOT_OPERATOR_DESC
title: DML_ONE_HOT_OPERATOR_DESC
description: Describes a DirectML operator that generates a tensor with each element filled with two values&mdash;either an 'on' or an 'off' value.
tech.root: directml
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
 - DML_ONE_HOT_OPERATOR_DESC
f1_keywords:
 - directml/DML_ONE_HOT_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Describes a DirectML operator that generates a tensor with each element filled with two values&mdash;either an 'on' or an 'off' value. The 'on'/'off' values aren't limited to Boolean `true` and `false`, but whatever two values are contained in *ValuesTensor*.

The output tensor is one additional dimension larger than the input indices tensor, inserted along the desired axis. Indices out of bounds are ignored (leaving just 'off' values along that sliver).

## -struct-fields

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the indices.

### -field ValuesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the values.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis dimension to add to *OutputTensor*.

## -remarks

## -see-also
