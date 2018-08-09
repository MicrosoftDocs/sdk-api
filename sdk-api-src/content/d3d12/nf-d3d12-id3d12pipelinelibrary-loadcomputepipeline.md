---
UID: NF:d3d12.ID3D12PipelineLibrary.LoadComputePipeline
title: ID3D12PipelineLibrary::LoadComputePipeline
author: windows-sdk-content
description: Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents.
old-location: direct3d12\id3d12pipelinelibrary_loadcomputepipeline.htm
old-project: direct3d12
ms.assetid: 8295D6E3-8353-46AD-A741-170244495F8B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12PipelineLibrary interface,LoadComputePipeline method, ID3D12PipelineLibrary.LoadComputePipeline, ID3D12PipelineLibrary::LoadComputePipeline, LoadComputePipeline, LoadComputePipeline method, LoadComputePipeline method,ID3D12PipelineLibrary interface, d3d12/ID3D12PipelineLibrary::LoadComputePipeline, direct3d12.id3d12pipelinelibrary_loadcomputepipeline
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
 - d3d12.dll
api_name:
 - ID3D12PipelineLibrary.LoadComputePipeline
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12PipelineLibrary::LoadComputePipeline


## -description


Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. 



## -parameters




### -param pName [in]

Type: <b>LPCWSTR</b>

The unique name of the PSO.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>*</b>

Specifies a description of the required PSO in a <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure. This input description is matched against the data in the current library database, and stored in order to prevent duplication of PSO contents.


### -param riid

Type: <b>REFIID</b>

Specifies a REFIID for the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> object. Typically set this, and the following parameter, with the macro <code>IID_PPV_ARGS(&amp;PSO1)</code>, where <i>PSO1</i> is the name of the object.


### -param ppPipelineState [out]

Type: <b>void**</b>

Specifies a pointer that will reference the returned PSO.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if the name doesn’t exist, or if the input description doesn’t match the data in the library, and E_OUTOFMEMORY if unable to allocate the return PSO. 





## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a>
 

 

