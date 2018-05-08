---
UID: NF:d3d12.ID3D12Device2.CreatePipelineState
title: ID3D12Device2::CreatePipelineState
author: windows-driver-content
description: Creates a pipeline state object from a pipeline state stream description.
old-location: direct3d12\id3d12device2_createpipelinestate.htm
old-project: direct3d12
ms.assetid: 90557451-CB7A-4F05-8BDB-B611FE034CBB
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: CreatePipelineState, CreatePipelineState method, CreatePipelineState method,ID3D12Device2 interface, ID3D12Device2 interface,CreatePipelineState method, ID3D12Device2.CreatePipelineState, ID3D12Device2::CreatePipelineState, d3d12/ID3D12Device2::CreatePipelineState, direct3d12.id3d12device2_createpipelinestate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12Device2.CreatePipelineState
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device2::CreatePipelineState


## -description


Creates a pipeline state object from a pipeline state stream description.


## -parameters




### -param pDesc

Type: <b>const <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a>*</b>

The address of a <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a> structure that describes the pipeline state.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the pipeline state interface (<a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>).

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the pipeline state can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D12PipelineState) will get the <b>GUID</b> of the interface to a pipeline state.


### -param ppPipelineState [out]

Type: <b>void**</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_COM_Outptr_</code>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> interface for the pipeline state object.

The pipeline state object is an immutable state object. It contains no methods.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object. See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.




## -remarks



This function takes the pipeline description as a <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a> and combines the functionality of the <a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">ID3D12Device::CreateGraphicsPipelineState</a> and <a href="https://msdn.microsoft.com/FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57">ID3D12Device::CreateComputePipelineState</a> functions, which take their pipeline description as the less-flexible <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structs, respectively.




## -see-also




<a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">ID3D12Device2</a>
 

 

