---
UID: NS:directml.DML_TENSOR_DESC
title: DML_TENSOR_DESC
description: A generic container for a DirectML tensor description.
helpviewer_keywords: ["DML_TENSOR_DESC","DML_TENSOR_DESC structure","direct3d12.dml_tensor_desc","directml/DML_TENSOR_DESC"]
old-location: direct3d12\dml_tensor_desc.htm
tech.root: directml
ms.assetid: 5F47CAC2-3896-4432-95BE-E28BE6D7566E
ms.date: 12/5/2018
ms.keywords: DML_TENSOR_DESC, DML_TENSOR_DESC structure, direct3d12.dml_tensor_desc, directml/DML_TENSOR_DESC
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
 - DML_TENSOR_DESC
 - directml/DML_TENSOR_DESC
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
 - DML_TENSOR_DESC
---

## -description

A generic container for a DirectML tensor description.

## -struct-fields

### -field Type

Type: [**DML_TENSOR_TYPE**](./ne-directml-dml_tensor_type.md)

The type of the tensor description. See <a href="/windows/win32/api/directml/ne-directml-dml_tensor_type">DML_TENSOR_TYPE</a> for the available types.

### -field Desc

Type: <b>const void*</b>

A pointer to the tensor description. The type of the pointed-to struct must match the value specified in <i>Type</i>.
