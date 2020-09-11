---
UID: NS:directml.DML_REDUCE_OPERATOR_DESC
title: DML_REDUCE_OPERATOR_DESC
description: Describes a DirectML operator that performs the specified reduction function on the input.
helpviewer_keywords: ["DML_REDUCE_OPERATOR_DESC","DML_REDUCE_OPERATOR_DESC structure","direct3d12.dml_reduce_operator_desc","directml/DML_REDUCE_OPERATOR_DESC"]
old-location: direct3d12\dml_reduce_operator_desc.htm
tech.root: directml
ms.assetid: 6C390A1A-7AA3-4B24-8DC7-A34E6FBE6320
ms.date: 12/5/2018
ms.keywords: DML_REDUCE_OPERATOR_DESC, DML_REDUCE_OPERATOR_DESC structure, direct3d12.dml_reduce_operator_desc, directml/DML_REDUCE_OPERATOR_DESC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_REDUCE_OPERATOR_DESC
 - directml/DML_REDUCE_OPERATOR_DESC
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
 - DML_REDUCE_OPERATOR_DESC
---

# DML_REDUCE_OPERATOR_DESC structure


## -description

Describes a DirectML operator that performs the specified reduction function on the input.

## -struct-fields

### -field Function

Type: [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function)

A <a href="https://msdn.microsoft.com/538BAB2E-C7AE-4A9E-AD87-4BDEEB677504">DML_REDUCE_FUNCTION</a> value specifying the reduce function to apply to the input.

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field AxisCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of axes. This field determines the size of the <i>Axes</i> array.

### -field Axes

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the axes along which to reduce.

