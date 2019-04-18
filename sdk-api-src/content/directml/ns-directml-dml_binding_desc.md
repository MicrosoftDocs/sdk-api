---
UID: NS:directml.DML_BINDING_DESC
title: DML_BINDING_DESC
author: windows-sdk-content
description: Contains the description of a binding so that you can add it to the binding table via a call to one of the IDMLBindingTable methods.
old-location: direct3d12\dml_binding_desc.htm
tech.root: direct3d12
ms.assetid: 80362AF6-148B-4C2E-8210-BC559BF58D12
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_BINDING_DESC, DML_BINDING_DESC structure, direct3d12.dml_binding_desc, directml/DML_BINDING_DESC
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_BINDING_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_BINDING_DESC structure


## -description






Contains the description of a binding so that you can add it to the binding table via a call to one of the [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable) methods.

 A binding can refer to an input or an output tensor resource, or to a persistent or a temporary resource, and there are methods on [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable) to bind each kind. The type of the structure pointed to by <i>Desc</i> depends on the value of <i>Type</i>.


## -struct-fields




### -field Type

Type: [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type)

A [DML_BINDING_TYPE](/windows/desktop/api/directml/ne-directml-dml_binding_type) specifying the type of the binding; whether it refers to a single buffer, or to an array of buffers.


### -field Desc

Type: <b>const void*</b>

A pointer to a constant structure whose type depends on the value <i>Type</i>. If <i>Type</i> is [DML_BINDING_TYPE_BUFFER](/windows/desktop/api/directml/ne-directml-dml_binding_type), then <i>Desc</i> should point to a [DML_BUFFER_BINDING](/windows/desktop/api/directml/ns-directml-dml_buffer_binding). If <i>Type</i> is <b><b>DML_BINDING_TYPE_BUFFER_ARRAY</b></b>, then <i>Desc</i> should point to a [DML_BUFFER_ARRAY_BINDING](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding).


## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>



[IDMLBindingTable::BindInputs](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs)



[IDMLBindingTable::BindOutputs](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)



[IDMLBindingTable::BindPersistentResource](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource)



[IDMLBindingTable::BindTemporaryResource](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource)
 

 

