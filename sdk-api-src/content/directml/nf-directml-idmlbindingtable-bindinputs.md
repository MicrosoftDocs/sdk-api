---
UID: NF:directml.IDMLBindingTable.BindInputs
title: IDMLBindingTable::BindInputs
description: Binds a set of resources as input tensors.
helpviewer_keywords: ["BindInputs","BindInputs method","BindInputs method","IDMLBindingTable interface","IDMLBindingTable interface","BindInputs method","IDMLBindingTable.BindInputs","IDMLBindingTable::BindInputs","direct3d12.idmlbindingtable_bindinputs","directml/IDMLBindingTable::BindInputs"]
old-location: direct3d12\idmlbindingtable_bindinputs.htm
tech.root: directml
ms.assetid: 125E5CBE-8ADF-4725-9F1D-66C38CD7A567
ms.date: 12/5/2018
ms.keywords: BindInputs, BindInputs method, BindInputs method,IDMLBindingTable interface, IDMLBindingTable interface,BindInputs method, IDMLBindingTable.BindInputs, IDMLBindingTable::BindInputs, direct3d12.idmlbindingtable_bindinputs, directml/IDMLBindingTable::BindInputs
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLBindingTable::BindInputs
 - directml/IDMLBindingTable::BindInputs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLBindingTable.BindInputs
---

# IDMLBindingTable::BindInputs


## -description

Binds a set of resources as input tensors.

If binding for a compiled operator, the number of bindings must exactly match the number of inputs of the operator, including optional tensors. This can be determined from the operator description used to create the operator. If too many or too few bindings are provided, device removal will occur. For optional tensors, you may use [DML_BINDING_TYPE_NONE](/windows/win32/api/directml/ne-directml-dml_binding_type) to specify 'no binding'. Otherwise, the binding type must match the tensor type when the operator was created.

For operator initializers, input bindings are expected to be of type [DML_BINDING_TYPE_BUFFER_ARRAY](/windows/win32/api/directml/ne-directml-dml_binding_type) with one input binding per operator to initialize, supplied in the order that you specified the operators during creation or reset of the initializer. Each buffer array should have a size equal to the number of inputs of its corresponding operator to initialize. Input tensors that had the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag set should be bound during initialize&mdash;otherwise, nothing should be bound for that tensor. If there is nothing to be bound as input for initialization of an operator (that is, there are no tensors with the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag set) then you may supply `nullptr` or an empty [DML_BUFFER_ARRAY_BINDING](/windows/win32/api/directml/ns-directml-dml_buffer_array_binding) to indicate 'no binding'.

To unbind all input resources, supply a *rangeCount* of 0, and a value of `nullptr` for *bindings*.

If an input tensor has the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag set, it may only be bound when executing an operator initializer. Otherwise, if the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag is not set, the opposite is true&mdash;the input tensor must not be bound when executing the initializer, but must be bound when executing the operator itself.

All buffers being bound as input must have heap type [D3D12_HEAP_TYPE_DEFAULT](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type), except when the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag is set. If the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) is set for a tensor that is being bound as input for an initializer, the buffer's heap type may be either [D3D12_HEAP_TYPE_DEFAULT](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) or [D3D12_HEAP_TYPE_UPLOAD](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type).

Each binding is not required to point to a unique resource. It is legal, for example, to supply all inputs as suballocations from the same Direct3D 12 buffer resource. Ranges for inputs are permitted to overlap. No Direct3D 12 resource bound for input may simultaneously be bound for output, except if the operator explicitly permits in-place execution. If using in-place execution, the input and output tensors must have the exact same sizes, strides, and total tensor size. Additionally, the input and output bindings must have the exact same offset size.

## -parameters

### -param bindingCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This parameter determines the size of the *bindings* array (if provided).

### -param bindings [in, optional]

Type: **const [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc)\***

An optional pointer to a constant array of [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc) containing descriptions of the tensor resources to bind.

## -see-also

<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>

<a href="/windows/win32/api/directml/nn-directml-idmlbindingtable">IDMLBindingTable</a>
