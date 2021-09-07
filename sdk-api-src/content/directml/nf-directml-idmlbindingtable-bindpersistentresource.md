---
UID: NF:directml.IDMLBindingTable.BindPersistentResource
title: IDMLBindingTable::BindPersistentResource
description: Binds a buffer as a persistent resource. You can determine the required size of this buffer range by calling IDMLDispatchable::GetBindingProperties.
helpviewer_keywords: ["BindPersistentResource","BindPersistentResource method","BindPersistentResource method","IDMLBindingTable interface","IDMLBindingTable interface","BindPersistentResource method","IDMLBindingTable.BindPersistentResource","IDMLBindingTable::BindPersistentResource","direct3d12.idmlbindingtable_bindpersistentresource","directml/IDMLBindingTable::BindPersistentResource"]
old-location: direct3d12\idmlbindingtable_bindpersistentresource.htm
tech.root: directml
ms.assetid: 9812B5C9-6E3E-4CAB-827F-C59A98F07F91
ms.date: 12/5/2018
ms.keywords: BindPersistentResource, BindPersistentResource method, BindPersistentResource method,IDMLBindingTable interface, IDMLBindingTable interface,BindPersistentResource method, IDMLBindingTable.BindPersistentResource, IDMLBindingTable::BindPersistentResource, direct3d12.idmlbindingtable_bindpersistentresource, directml/IDMLBindingTable::BindPersistentResource
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
 - IDMLBindingTable::BindPersistentResource
 - directml/IDMLBindingTable::BindPersistentResource
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
 - IDMLBindingTable.BindPersistentResource
---

# IDMLBindingTable::BindPersistentResource


## -description

Binds a buffer as a persistent resource. You can determine the required size of this buffer range by calling [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties).

If the binding properties for the operator specify a size of zero for the persistent resource, then you may supply <b>nullptr</b> to this method (which indicates no resource to bind). Otherwise, a binding of type [DML_BINDING_TYPE_BUFFER](/windows/win32/api/directml/ne-directml-dml_binding_type) must be supplied that is at least as large as the required <b>PersistentResourceSize</b> returned by [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties).

Unlike the temporary resource, the persistent resource's contents and lifetime must persist as long as the compiled operator does. That is, if an operator requires a persistent resource, then your application must supply it during initialization and subsequently also supply it to all future executes of the operator without modifying its contents.

The persistent resource is typically used by DirectML to store lookup tables or other long-lived data that is computed during initialization of an operator and reused on future executions of that operator.

As the persistent resource's data is opaque, once initialized it cannot be copied or moved to another buffer.

The persistent resource is only written to during initialization of an operator and is thereafter immutable; all subsequent executions are guaranteed not to write to the persistent resource.

The supplied buffer range to be bound as the persistent buffer must have its start offset aligned to [DML_PERSISTENT_BUFFER_ALIGNMENT](/windows/desktop/direct3d12/direct3d-directml-constants). The type of the heap underlying the buffer must be <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE_DEFAULT</a>.

## -parameters

### -param binding [in, optional]

Type: <b>const [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc)*</b>

An optional pointer to a [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc) containing the description of a tensor resource to bind.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>

[IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable)