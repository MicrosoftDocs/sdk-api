---
UID: NF:directml.IDMLCommandRecorder.RecordDispatch
title: IDMLCommandRecorder::RecordDispatch
description: Records execution of a dispatchable object (an operator initializer, or a compiled operator) onto a command list.
helpviewer_keywords: ["IDMLCommandRecorder interface","RecordDispatch method","IDMLCommandRecorder.RecordDispatch","IDMLCommandRecorder::RecordDispatch","RecordDispatch","RecordDispatch method","RecordDispatch method","IDMLCommandRecorder interface","direct3d12.idmlcommandrecorder_recorddispatch","directml/IDMLCommandRecorder::RecordDispatch"]
old-location: direct3d12\idmlcommandrecorder_recorddispatch.htm
tech.root: directml
ms.assetid: E76A4CD7-A6A9-4B3F-9E81-3C1BAEB32657
ms.date: 12/5/2018
ms.keywords: IDMLCommandRecorder interface,RecordDispatch method, IDMLCommandRecorder.RecordDispatch, IDMLCommandRecorder::RecordDispatch, RecordDispatch, RecordDispatch method, RecordDispatch method,IDMLCommandRecorder interface, direct3d12.idmlcommandrecorder_recorddispatch, directml/IDMLCommandRecorder::RecordDispatch
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
 - IDMLCommandRecorder::RecordDispatch
 - directml/IDMLCommandRecorder::RecordDispatch
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
 - IDMLCommandRecorder.RecordDispatch
---

# IDMLCommandRecorder::RecordDispatch


## -description

Records execution of a dispatchable object (an operator initializer, or a compiled operator) onto a command
       list.

This method doesn't submit the execution to the GPU; it merely records it onto the command list. You are responsible for closing the command list and submitting it to the Direct3D 12 command queue.

Prior to execution of this call on the GPU, all resources bound must be in the <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a> state, or a
        state implicitly promotable to <b>D3D12_RESOURCE_STATE_UNORDERED_ACCESS</b>, such as <b>D3D12_RESOURCE_STATE_COMMON</b>. After this call completes, the resources
        remain in the <b>D3D12_RESOURCE_STATE_UNORDERED_ACCESS</b> state. The only exception to this is for upload heaps bound when executing an
        operator initializer and while one or more tensors has the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag set. In that case, any
        upload heaps bound for input must be in the <b>D3D12_RESOURCE_STATE_GENERIC_READ</b> state and will remain in that state, as required by
        all upload heaps.

This method resets the following state on the command list.
<ul>
<li>Compute root signature</li>
<li>Pipeline state</li>
</ul>No other command list state is modified.

Although this method takes a binding table representing the resources to bind to the pipeline, it doesn't
        set the descriptor heaps containing the descriptors themselves. Therefore, your application is responsible for
        calling <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps">ID3D12GraphicsCommandList::SetDescriptorHeaps</a> to bind the correct descriptor heaps to the pipeline.

If [DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE](/windows/win32/api/directml/ne-directml-dml_execution_flags) was not set when compiling the operator, then all bindings must
        be set on the binding table before <b>RecordDispatch</b> is called, otherwise the behavior is undefined. Otherwise,
        if the <b>_DESCRIPTORS_VOLATILE</b> flag is set, binding of resources may be deferred until the Direct3D 12 command list is
        submitted to the command queue for execution.

This method acts logically like a call to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch">ID3D12GraphicsCommandList::Dispatch</a>. As such, unordered access view (UAV) barriers are
        necessary to ensure correct ordering if there are data dependencies between dispatches. This method does not
        insert UAV barriers on input nor output resources. Your application must ensure that the correct UAV barriers
        are performed on any inputs if their contents depend on an upstream dispatch, and on any outputs if there are
        downstream dispatches that depend on those outputs.

This method doesn't hold references to any of the interfaces passed in. It is your responsibility to
        ensure that the [IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable) object is not released until all dispatches using it have completed execution
        on the GPU.

## -parameters

### -param commandList

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>*</b>

A pointer to an <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a> interface representing the command list to record the execution into. The command list must be open and must have type
          <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE_DIRECT</a> or <b>D3D12_COMMAND_LIST_TYPE_COMPUTE</b>.

### -param dispatchable

Type: <b>[IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable)*</b>

A pointer to an [IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable) interface representing the object (an operator initializer, or a compiled operator) whose execution will be recorded into the command list.

### -param bindings

Type: <b>[IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable)*</b>

A pointer to an [IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable) interface representing the bindings to use for executing the dispatchable object. If the [DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE](/windows/win32/api/directml/ne-directml-dml_execution_flags)
          flag was not set, then you must fill out all required bindings, otherwise an error will result.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>

[IDMLCommandRecorder](/windows/win32/api/directml/nn-directml-idmlcommandrecorder)
