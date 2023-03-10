---
UID: NF:directml.IDMLBindingTable.BindTemporaryResource
title: IDMLBindingTable::BindTemporaryResource
description: Binds a buffer to use as temporary scratch memory. You can determine the required size of this buffer range by calling IDMLDispatchable::GetBindingProperties.
helpviewer_keywords: ["BindTemporaryResource","BindTemporaryResource method","BindTemporaryResource method","IDMLBindingTable interface","IDMLBindingTable interface","BindTemporaryResource method","IDMLBindingTable.BindTemporaryResource","IDMLBindingTable::BindTemporaryResource","direct3d12.idmlbindingtable_bindtemporaryresource","directml/IDMLBindingTable::BindTemporaryResource"]
old-location: direct3d12\idmlbindingtable_bindtemporaryresource.htm
tech.root: directml
ms.assetid: B4673D07-997A-4D9A-B0B8-B615687BFD6C
ms.date: 12/5/2018
ms.keywords: BindTemporaryResource, BindTemporaryResource method, BindTemporaryResource method,IDMLBindingTable interface, IDMLBindingTable interface,BindTemporaryResource method, IDMLBindingTable.BindTemporaryResource, IDMLBindingTable::BindTemporaryResource, direct3d12.idmlbindingtable_bindtemporaryresource, directml/IDMLBindingTable::BindTemporaryResource
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
 - IDMLBindingTable::BindTemporaryResource
 - directml/IDMLBindingTable::BindTemporaryResource
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
 - IDMLBindingTable.BindTemporaryResource
---

# IDMLBindingTable::BindTemporaryResource


## -description

Binds a buffer to use as temporary scratch memory. You can determine the required size of this buffer range by calling [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties).

If the binding properties for the [IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable) specify a size of zero for the temporary resource, then you may
        supply <b>nullptr</b> to this method (which indicates no resource to bind). Otherwise, a binding of type
        [DML_BINDING_TYPE_BUFFER](/windows/win32/api/directml/ne-directml-dml_binding_type) must be supplied that is at least as large as the required <b>TemporaryResourceSize</b>
        returned by [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties).

The temporary resource is typically used as scratch memory during execution of an operator. The contents
        of a temporary resource need not be defined prior to execution. For example, DirectML doesn't require that
        you zero the contents of the temporary resource prior to binding or executing an operator.

You don't need to preserve the contents of the temporary buffer, and your application is free to overwrite or
        reuse its contents as soon as execution of an operator or initializer completes on the GPU. This is in contrast
        to a persistent resource, whose contents must be preserved and lifetime extended for the lifetime of the
        operator.

The supplied buffer range to be bound as the temporary buffer must have its start offset aligned to
        [DML_TEMPORARY_BUFFER_ALIGNMENT](/windows/desktop/direct3d12/direct3d-directml-constants). The type of the heap underlying the buffer must be <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE_DEFAULT</a>.

## -parameters

### -param binding [in, optional]

Type: <b>const [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc)*</b>

An optional pointer to a [DML_BINDING_DESC](/windows/win32/api/directml/ns-directml-dml_binding_desc) containing the description of a tensor resource to bind.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>

[IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable)
