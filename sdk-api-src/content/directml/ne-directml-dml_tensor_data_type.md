---
UID: NE:directml.DML_TENSOR_DATA_TYPE
title: DML_TENSOR_DATA_TYPE
description: Specifies the data type of the values in a tensor. DirectML operators may not support all data types; see the documentation for each specific operator to find which data types it supports.
helpviewer_keywords: ["DML_TENSOR_DATA_TYPE","DML_TENSOR_DATA_TYPE enumeration","DML_TENSOR_DATA_TYPE_FLOAT16","DML_TENSOR_DATA_TYPE_FLOAT32","DML_TENSOR_DATA_TYPE_INT16","DML_TENSOR_DATA_TYPE_INT32","DML_TENSOR_DATA_TYPE_INT8","DML_TENSOR_DATA_TYPE_UINT16","DML_TENSOR_DATA_TYPE_UINT32","DML_TENSOR_DATA_TYPE_UINT8","DML_TENSOR_DATA_TYPE_UNKNOWN","direct3d12.dml_tensor_data_type","directml/DML_TENSOR_DATA_TYPE","directml/DML_TENSOR_DATA_TYPE_FLOAT16","directml/DML_TENSOR_DATA_TYPE_FLOAT32","directml/DML_TENSOR_DATA_TYPE_INT16","directml/DML_TENSOR_DATA_TYPE_INT32","directml/DML_TENSOR_DATA_TYPE_INT8","directml/DML_TENSOR_DATA_TYPE_UINT16","directml/DML_TENSOR_DATA_TYPE_UINT32","directml/DML_TENSOR_DATA_TYPE_UINT8","directml/DML_TENSOR_DATA_TYPE_UNKNOWN"]
old-location: direct3d12\dml_tensor_data_type.htm
tech.root: directml
ms.assetid: 28B75489-EDD9-4D06-881B-E7D547C56418
ms.date: 12/5/2018
ms.keywords: DML_TENSOR_DATA_TYPE, DML_TENSOR_DATA_TYPE enumeration, DML_TENSOR_DATA_TYPE_FLOAT16, DML_TENSOR_DATA_TYPE_FLOAT32, DML_TENSOR_DATA_TYPE_INT16, DML_TENSOR_DATA_TYPE_INT32, DML_TENSOR_DATA_TYPE_INT8, DML_TENSOR_DATA_TYPE_UINT16, DML_TENSOR_DATA_TYPE_UINT32, DML_TENSOR_DATA_TYPE_UINT8, DML_TENSOR_DATA_TYPE_UNKNOWN, direct3d12.dml_tensor_data_type, directml/DML_TENSOR_DATA_TYPE, directml/DML_TENSOR_DATA_TYPE_FLOAT16, directml/DML_TENSOR_DATA_TYPE_FLOAT32, directml/DML_TENSOR_DATA_TYPE_INT16, directml/DML_TENSOR_DATA_TYPE_INT32, directml/DML_TENSOR_DATA_TYPE_INT8, directml/DML_TENSOR_DATA_TYPE_UINT16, directml/DML_TENSOR_DATA_TYPE_UINT32, directml/DML_TENSOR_DATA_TYPE_UINT8, directml/DML_TENSOR_DATA_TYPE_UNKNOWN
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
 - DML_TENSOR_DATA_TYPE
 - directml/DML_TENSOR_DATA_TYPE
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
 - DML_TENSOR_DATA_TYPE
---

## -description

Specifies the data type of the values in a tensor. DirectML operators may not support all data types; see the documentation for each specific operator to find which data types it supports.

## -enum-fields

### -field DML_TENSOR_DATA_TYPE_UNKNOWN

Indicates an unknown data type. This value is never valid.

### -field DML_TENSOR_DATA_TYPE_FLOAT32

Indicates a 32-bit floating-point data type.

### -field DML_TENSOR_DATA_TYPE_FLOAT16

Indicates a 16-bit floating-point data type.

### -field DML_TENSOR_DATA_TYPE_UINT32

Indicates a 32-bit unsigned integer data type.

### -field DML_TENSOR_DATA_TYPE_UINT16

Indicates a 16-bit unsigned integer data type.

### -field DML_TENSOR_DATA_TYPE_UINT8

Indicates a 8-bit unsigned integer data type.

### -field DML_TENSOR_DATA_TYPE_INT32

Indicates a 32-bit signed integer data type.

### -field DML_TENSOR_DATA_TYPE_INT16

Indicates a 16-bit signed integer data type.

### -field DML_TENSOR_DATA_TYPE_INT8

Indicates a 8-bit signed integer data type.
