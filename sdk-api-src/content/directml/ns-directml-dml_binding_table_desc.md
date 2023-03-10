---
UID: NS:directml.DML_BINDING_TABLE_DESC
title: DML_BINDING_TABLE_DESC
description: Specifies parameters to IDMLDevice::CreateBindingTable and IDMLBindingTable::Reset.
helpviewer_keywords: ["DML_BINDING_TABLE_DESC","DML_BINDING_TABLE_DESC structure","direct3d12.dml_binding_table_desc","directml/DML_BINDING_TABLE_DESC"]
old-location: direct3d12\dml_binding_table_desc.htm
tech.root: directml
ms.assetid: 4ABA8CBB-C298-4F98-8156-CD81F83BB657
ms.date: 12/5/2018
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
 - DML_BINDING_TABLE_DESC
 - directml/DML_BINDING_TABLE_DESC
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
 - DML_BINDING_TABLE_DESC
---

## -description

Specifies parameters to [IDMLDevice::CreateBindingTable](/windows/win32/api/directml/nf-directml-idmldevice-createbindingtable) and [IDMLBindingTable::Reset](/windows/win32/api/directml/nf-directml-idmlbindingtable-reset).

## -struct-fields

### -field Dispatchable

Type: <b>[IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable)*</b>

A pointer to an [IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable) interface representing the dispatchable object (an operator initializer, or a compiled operator) for which this binding table will represent the bindings—either an
        [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator) or an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer). The binding table maintains a strong reference to this
        interface pointer. This value may not be null.

### -field CPUDescriptorHandle

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A valid CPU descriptor handle representing the start of a range into a constant buffer view (CBV)/shader resource view (SRV)/ unordered access view (UAV) descriptor heap into which
        DirectML may write descriptors.

### -field GPUDescriptorHandle

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A valid GPU descriptor handle representing the start of a range into a constant buffer view (CBV)/shader resource view (SRV)/ unordered access view (UAV) descriptor heap that DirectML may use to bind resources to the pipeline.

### -field SizeInDescriptors

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size of the binding table, in descriptors. This is the maximum number of descriptors that DirectML is
        permitted to write, from the start of both the supplied CPU and GPU descriptor handles. Call
        [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties) to determine the number of descriptors required to execute a
        dispatchable object.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>
