---
UID: NF:d3d12.ID3D12Device.CreateComputePipelineState
title: ID3D12Device::CreateComputePipelineState
author: windows-sdk-content
description: Creates a compute pipeline state object.
old-location: direct3d12\id3d12device_createcomputepipelinestate.htm
old-project: direct3d12
ms.assetid: FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: CreateComputePipelineState, CreateComputePipelineState method, CreateComputePipelineState method,ID3D12Device interface, ID3D12Device interface,CreateComputePipelineState method, ID3D12Device.CreateComputePipelineState, ID3D12Device::CreateComputePipelineState, d3d12/ID3D12Device::CreateComputePipelineState, direct3d12.id3d12device_createcomputepipelinestate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateComputePipelineState
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateComputePipelineState


## -description


Creates a compute pipeline state object.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure that describes compute pipeline state.
          


### -param riid

Type: <b>REFIID</b>


            The globally unique identifier (<b>GUID</b>) for the pipeline state interface (<a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the pipeline state can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12PipelineState) will get the <b>GUID</b> of the interface to a pipeline state.
          


### -param ppPipelineState [out]

Type: <b>void**</b>


            A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> interface for the pipeline state object.
            The pipeline state object is an immutable state object.  It contains no methods.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object.
              See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
            




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

