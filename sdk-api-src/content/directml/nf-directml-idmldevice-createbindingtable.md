---
UID: NF:directml.IDMLDevice.CreateBindingTable
title: IDMLDevice::CreateBindingTable
author: windows-sdk-content
description: Creates a binding table, which is an object that can be used to bind resources (such as tensors) to the pipeline.
old-location: direct3d12\idmldevice_createbindingtable.htm
tech.root: direct3d12
ms.assetid: 04E981C1-833C-4359-A30F-A2727DD015BC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBindingTable, CreateBindingTable method, CreateBindingTable method,IDMLDevice interface, IDMLDevice interface,CreateBindingTable method, IDMLDevice.CreateBindingTable, IDMLDevice::CreateBindingTable, direct3d12.idmldevice_createbindingtable, directml/IDMLDevice::CreateBindingTable
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDevice.CreateBindingTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDevice::CreateBindingTable


## -description






Creates a binding table, which is an object that can be used to bind resources (such as tensors) to the pipeline.

The binding table wraps a range of an application-managed descriptor heap using the provided descriptor handles
        and count.  Binding tables are used by DirectML to manage the binding of resources by writing descriptors into
        the descriptor heap at the offset specified by the <b>CPUDescriptorHandle</b>, and binding those descriptors to the
        pipeline using the descriptors at the offset specified by the <b>GPUDescriptorHandle</b>. The order in which
        DirectML writes descriptors into the heap is unspecified, so your application must take care not to overwrite the
        descriptors wrapped by the binding table.

The supplied CPU and GPU descriptor handles may come from different heaps, however it is then your
        application's responsibility to ensure that the entire descriptor range referred to by the CPU descriptor
        handle is copied into the range referred to by the GPU descriptor handle prior to execution using this binding
        table.

The descriptor heap from which the handles are supplied must have type <a href="https://msdn.microsoft.com/E74C78BC-B0FC-473A-B4F3-434F50A55E9F">D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV</a>.
        Additionally, the heap referred to by the <b>GPUDescriptorHandle</b> must be a shader-visible descriptor heap.

You must not delete the heap referred to by the GPU descriptor handle until all work referencing it has
        completed execution on the GPU. You may, however, reset or release the binding table itself as soon as the
        dispatch has been recorded into the command list. Similar to the relationship between <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a> and
        <a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a>, the [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable) doesn't own the underlying memory referenced by the descriptor
        handles. Rather, the <a href="https://msdn.microsoft.com/B6FF011B-3FED-425B-B9D5-A823E6915FD5">ID3D12DescriptorHeap</a> does. Therefore, you're permitted to reset or release a DirectML binding table before work using the binding table has completed execution on the GPU.


## -parameters




### -param desc [in, optional]

Type: <b>const [DML_BINDING_TABLE_DESC](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc)*</b>

An optional pointer to a [DML_BINDING_TABLE_DESC](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) containing the binding table parameters. This may be <b>nullptr</b>, indicating an empty binding table.


### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable).


### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the binding table. This is the address of a pointer to an [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable), representing  the binding table created.


## -returns



Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.




## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>



[IDMLDevice](/windows/desktop/api/directml/nn-directml-idmldevice)
 

 

