---
UID: NN:directml.IDMLBindingTable
title: IDMLBindingTable
description: Wraps a range of an application-managed descriptor heap, and is used by DirectML to create bindings for resources. To create this object, call IDMLDevice::CreateBindingTable.
helpviewer_keywords: ["IDMLBindingTable","IDMLBindingTable interface","IDMLBindingTable interface","described","direct3d12.idmlbindingtable","directml/IDMLBindingTable"]
old-location: direct3d12\idmlbindingtable.htm
tech.root: directml
ms.assetid: ED3D6CCD-BBF5-4CA6-BA59-F8B3FEE40DA1
ms.date: 12/5/2018
ms.keywords: IDMLBindingTable, IDMLBindingTable interface, IDMLBindingTable interface,described, direct3d12.idmlbindingtable, directml/IDMLBindingTable
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
 - IDMLBindingTable
 - directml/IDMLBindingTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLBindingTable
---

# IDMLBindingTable interface


## -description

Wraps a range of an application-managed descriptor heap, and is used by DirectML to create bindings for resources. To create this object, call [IDMLDevice::CreateBindingTable](/windows/win32/api/directml/nf-directml-idmldevice-createbindingtable). The **IDMLBindingTable** interface inherits from [IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild).

The binding table is created over a range of CPU and GPU descriptor handles. When an IDMLBindingTable::Bind* method is called, DirectML writes one or more descriptors into the range of CPU descriptors. When you use the binding table during a call to [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch), DirectML binds the corresponding GPU descriptors to the pipeline.

The CPU and GPU descriptor handles aren't required to point to the same entries in a descriptor heap, however it is then your application's responsibility to ensure that the entire descriptor range referred to by the CPU descriptor handle is copied into the range referred to by the GPU descriptor handle prior to execution using this binding table.

It is your application's responsibility to perform correct synchronization between the CPU and GPU work that uses this binding table. For example, you must take care not to overwrite the bindings created by the binding table (for example, by calling Bind* again on the binding table, or by overwriting the descriptor heap manually) until all work using the binding table has completed execution on the GPU. In addition, since the binding table doesn't maintain a reference on the descriptor heap it writes into, you must not release the backing shader-visible descriptor heap until all work using that binding table has completed execution on the GPU.

The binding table is associated with exactly one dispatchable object (an operator initializer, or a compiled operator), and represents the bindings for that particular object. You can reuse a binding table by calling [IDMLBindingTable::Reset](/windows/win32/api/directml/nf-directml-idmlbindingtable-reset), however. Note that since the binding table doesn't own the descriptor heap itself, it is safe to call <b>Reset</b> and reuse the binding table for a different dispatchable object even before any outstanding executions have completed on the GPU.

The binding table doesn't keep strong references on any resources bound using it—your application must ensure that resources are not deleted while still in use by the GPU.

This object is not thread safe—your application must not call methods on the binding table simultaneously from different threads without synchronization.

## -see-also

[Binding in DirectML](/windows/ai/directml/dml-binding)

[IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild)
