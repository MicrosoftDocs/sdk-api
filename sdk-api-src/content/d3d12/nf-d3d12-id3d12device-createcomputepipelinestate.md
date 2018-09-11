---
UID: NF:d3d12.ID3D12Device.CreateComputePipelineState
title: ID3D12Device::CreateComputePipelineState
author: windows-sdk-content
description: Creates a compute pipeline state object.
old-location: direct3d12\id3d12device_createcomputepipelinestate.htm
tech.root: direct3d12
ms.assetid: FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateComputePipelineState, CreateComputePipelineState method, CreateComputePipelineState method,ID3D12Device interface, ID3D12Device interface,CreateComputePipelineState method, ID3D12Device.CreateComputePipelineState, ID3D12Device::CreateComputePipelineState, d3d12/ID3D12Device::CreateComputePipelineState, direct3d12.id3d12device_createcomputepipelinestate
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateComputePipelineState


## -description


Creates a compute pipeline state object.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn770350(v=VS.85).aspx">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn770350(v=VS.85).aspx">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure that describes compute pipeline state.
          


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the pipeline state interface (<a href="https://msdn.microsoft.com/en-us/library/Dn788705(v=VS.85).aspx">ID3D12PipelineState</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the pipeline state can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12PipelineState) will get the <b>GUID</b> of the interface to a pipeline state.
          


### -param ppPipelineState [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn788705(v=VS.85).aspx">ID3D12PipelineState</a> interface for the pipeline state object.
            The pipeline state object is an immutable state object.  It contains no methods.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object.
              See <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a> for other possible return values.
            




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>
 

 

