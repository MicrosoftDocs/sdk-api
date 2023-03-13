---
UID: NF:directml.IDMLBindingTable.BindOutputs
title: IDMLBindingTable::BindOutputs
description: Binds a set of resources as output tensors.
helpviewer_keywords: ["BindOutputs","BindOutputs method","BindOutputs method","IDMLBindingTable interface","IDMLBindingTable interface","BindOutputs method","IDMLBindingTable.BindOutputs","IDMLBindingTable::BindOutputs","direct3d12.idmlbindingtable_bindoutputs","directml/IDMLBindingTable::BindOutputs"]
old-location: direct3d12\idmlbindingtable_bindoutputs.htm
tech.root: directml
ms.assetid: DBAD9981-03CD-46EA-AD94-6781C6A25626
ms.date: 01/19/2021
ms.keywords: BindOutputs, BindOutputs method, BindOutputs method,IDMLBindingTable interface, IDMLBindingTable interface,BindOutputs method, IDMLBindingTable.BindOutputs, IDMLBindingTable::BindOutputs, direct3d12.idmlbindingtable_bindoutputs, directml/IDMLBindingTable::BindOutputs
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
 - IDMLBindingTable::BindOutputs
 - directml/IDMLBindingTable::BindOutputs
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
 - IDMLBindingTable.BindOutputs
---

## -description

Binds a set of resources as output tensors.

If binding for a compiled operator, the number of bindings must exactly match the number of inputs of the operator, including optional tensors. This can be determined from the operator description used to create the operator. If too many or too few bindings are provided, device removal will occur. For optional tensors, you may use [DML_BINDING_TYPE_NONE](/windows/win32/api/directml/ne-directml-dml_binding_type) to specify 'no binding'. Otherwise, the binding type must match the tensor type when the operator was created.

For operator initializers, the output bindings are the persistent resources of each operator, supplied in the order the operators were given when creating or resetting the initializer. If a particular operator does not require a persistent resource, you should prove an empty binding in that slot.

To unbind all input resources, supply a <i>rangeCount</i> of 0, and a value of <b>nullptr</b> for <i>bindings</i>.

The writable areas of two output tensors must not overlap with one another. The 'writable area' of an output buffer being bound is defined as being the start offset of the buffer range, up to the <i>TotalTensorSizeInBytes</i> as specified in the tensors description.

All buffers being bound as output must have heap type <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE_DEFAULT</a>.

## -parameters

### -param bindingCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This parameter determines the size of the <i>bindings</i> array (if provided).

### -param bindings [in, optional]

Type: <b>const [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc)*</b>

An optional pointer to a constant array of [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc) containing descriptions of the tensor resources to bind.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>

[IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable)