---
UID: NE:directml.DML_TENSOR_FLAGS
title: DML_TENSOR_FLAGS
description: Specifies additional options in a tensor description. Values can be bitwise OR'd together.
helpviewer_keywords: ["DML_TENSOR_FLAGS","DML_TENSOR_FLAGS enumeration","DML_TENSOR_FLAG_NONE","DML_TENSOR_FLAG_OWNED_BY_DML","direct3d12.dml_tensor_flags","directml/DML_TENSOR_FLAGS","directml/DML_TENSOR_FLAG_NONE","directml/DML_TENSOR_FLAG_OWNED_BY_DML"]
old-location: direct3d12\dml_tensor_flags.htm
tech.root: directml
ms.assetid: 61704FFD-51F8-4872-8EAA-110F64B908B3
ms.date: 12/5/2018
ms.keywords: DML_TENSOR_FLAGS, DML_TENSOR_FLAGS enumeration, DML_TENSOR_FLAG_NONE, DML_TENSOR_FLAG_OWNED_BY_DML, direct3d12.dml_tensor_flags, directml/DML_TENSOR_FLAGS, directml/DML_TENSOR_FLAG_NONE, directml/DML_TENSOR_FLAG_OWNED_BY_DML
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
 - DML_TENSOR_FLAGS
 - directml/DML_TENSOR_FLAGS
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
 - DML_TENSOR_FLAGS
---

## -description

Specifies additional options in a tensor description. Values can be bitwise OR'd together.

## -enum-fields

### -field DML_TENSOR_FLAG_NONE:0x0

No options are specified.

### -field DML_TENSOR_FLAG_OWNED_BY_DML:0x1

Indicates that the tensor data should be owned and managed by DirectML. The effect of this flag is that DirectML makes a copy of the tensor data during initialization of an operator, storing it in the persistent resource. This allows DirectML to perform reformatting of the tensor data into other, more efficient forms. Setting this flag may increase performance, but is typically only useful for tensors whose data doesn't change for the lifetime of the operator (for example, weight tensors).
      
This flag can only be used on input tensors.

When this flag is set on a particular tensor description, the corresponding tensor must be bound to the binding table during operator initialization, and not during execution. Attempting to bind the tensor during execution while this flag is set results in an error. This is the opposite of the default behavior (the behavior without the <b>DML_TENSOR_FLAG_OWNED_BY_DML</b> flag), where the tensor is expected to be bound during execution, and not during initialization.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>
