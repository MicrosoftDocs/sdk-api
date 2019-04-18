---
UID: NF:directml.IDMLCommandRecorder.RecordDispatch
title: IDMLCommandRecorder::RecordDispatch
author: windows-sdk-content
description: Records execution of a dispatchable object (an operator initializer, or a compiled operator) onto a command list.
old-location: direct3d12\idmlcommandrecorder_recorddispatch.htm
tech.root: direct3d12
ms.assetid: E76A4CD7-A6A9-4B3F-9E81-3C1BAEB32657
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLCommandRecorder interface,RecordDispatch method, IDMLCommandRecorder.RecordDispatch, IDMLCommandRecorder::RecordDispatch, RecordDispatch, RecordDispatch method, RecordDispatch method,IDMLCommandRecorder interface, direct3d12.idmlcommandrecorder_recorddispatch, directml/IDMLCommandRecorder::RecordDispatch
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
 - IDMLCommandRecorder.RecordDispatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLCommandRecorder::RecordDispatch


## -description







       Records execution of a dispatchable object (an operator initializer, or a compiled operator) onto a command
       list.

This method doesn't submit the execution to the GPU; it merely records it onto the command list. You are responsible for closing the command list and submitting it to the Direct3D 12 command queue.

Prior to execution of this call on the GPU, all resources bound must be in the <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a> state, or a
        state implicitly promotable to <b>D3D12_RESOURCE_STATE_UNORDERED_ACCESS</b>, such as <b>D3D12_RESOURCE_STATE_COMMON</b>. After this call completes, the resources
        remain in the <b>D3D12_RESOURCE_STATE_UNORDERED_ACCESS</b> state. The only exception to this is for upload heaps bound when executing an
        operator initializer and while one or more tensors has the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) flag set. In that case, any
        upload heaps bound for input must be in the <b>D3D12_RESOURCE_STATE_GENERIC_READ</b> state and will remain in that state, as required by
        all upload heaps.

This method resets the following state on the command list.
<ul>
<li>Compute root signature</li>
<li>Pipeline state</li>
</ul>No other command list state is modified.

Although this method takes a binding table representing the resources to bind to the pipeline, it doesn't
        set the descriptor heaps containing the descriptors themselves. Therefore, your application is responsible for
        calling <a href="https://msdn.microsoft.com/EE475B68-1DCA-44D4-994E-717D40F47DFA">ID3D12GraphicsCommandList::SetDescriptorHeaps</a> to bind the correct descriptor heaps to the pipeline.

If [DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE](/windows/desktop/api/directml/ne-directml-dml_execution_flags) was not set when compiling the operator, then all bindings must
        be set on the binding table before <b>RecordDispatch</b> is called, otherwise the behavior is undefined. Otherwise,
        if the <b>_DESCRIPTORS_VOLATILE</b> flag is set, binding of resources may be deferred until the Direct3D 12 command list is
        submitted to the command queue for execution.

This method acts logically like a call to <a href="https://msdn.microsoft.com/948EE430-6B34-473D-9B5F-1C78CECFBF6F">ID3D12GraphicsCommandList::Dispatch</a>. As such, unordered access view (UAV) barriers are
        necessary to ensure correct ordering if there are data dependencies between dispatches. This method does not
        insert UAV barriers on input nor output resources. Your application must ensure that the correct UAV barriers
        are performed on any inputs if their contents depend on an upstream dispatch, and on any outputs if there are
        downstream dispatches that depend on those outputs.

This method doesn't hold references to any of the interfaces passed in. It is your responsibility to
        ensure that the [IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable) object is not released until all dispatches using it have completed execution
        on the GPU.


## -parameters




### -param commandList

Type: <b><a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/1E0359CC-0F53-4C82-9F1A-092F6F72EE20">ID3D12CommandList</a> interface representing the command list to record the execution into. The command list must be open and must have type
          <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE_DIRECT</a> or <b>D3D12_COMMAND_LIST_TYPE_COMPUTE</b>.


### -param dispatchable

Type: <b>[IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable)*</b>

A pointer to an [IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable) interface representing the object (an operator initializer, or a compiled operator) whose execution will be recorded into the command list.


### -param bindings

Type: <b>[IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable)*</b>

A pointer to an [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable) interface representing the bindings to use for executing the dispatchable object. If the [DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE](/windows/desktop/api/directml/ne-directml-dml_execution_flags)
          flag was not set, then you must fill out all required bindings, otherwise an error will result.


## -returns



This method does not return a value.




## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>



[IDMLCommandRecorder](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder)
 

 

