---
UID: NF:d3d12.ID3D12PipelineLibrary.LoadComputePipeline
title: ID3D12PipelineLibrary::LoadComputePipeline (d3d12.h)
description: Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents.
helpviewer_keywords: ["ID3D12PipelineLibrary interface","LoadComputePipeline method","ID3D12PipelineLibrary.LoadComputePipeline","ID3D12PipelineLibrary::LoadComputePipeline","LoadComputePipeline","LoadComputePipeline method","LoadComputePipeline method","ID3D12PipelineLibrary interface","d3d12/ID3D12PipelineLibrary::LoadComputePipeline","direct3d12.id3d12pipelinelibrary_loadcomputepipeline"]
old-location: direct3d12\id3d12pipelinelibrary_loadcomputepipeline.htm
tech.root: direct3d12
ms.assetid: 8295D6E3-8353-46AD-A741-170244495F8B
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineLibrary interface,LoadComputePipeline method, ID3D12PipelineLibrary.LoadComputePipeline, ID3D12PipelineLibrary::LoadComputePipeline, LoadComputePipeline, LoadComputePipeline method, LoadComputePipeline method,ID3D12PipelineLibrary interface, d3d12/ID3D12PipelineLibrary::LoadComputePipeline, direct3d12.id3d12pipelinelibrary_loadcomputepipeline
f1_keywords:
- d3d12/ID3D12PipelineLibrary.LoadComputePipeline
dev_langs:
- c++
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12PipelineLibrary.LoadComputePipeline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12PipelineLibrary::LoadComputePipeline


## -description


Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. 



## -parameters




### -param pName [in]

Type: <b>LPCWSTR</b>

The unique name of the PSO.


### -param pDesc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>*</b>

Specifies a description of the required PSO in a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure. This input description is matched against the data in the current library database, and stored in order to prevent duplication of PSO contents.


### -param riid

Type: <b>REFIID</b>

Specifies a REFIID for the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> object. Typically set this, and the following parameter, with the macro <code>IID_PPV_ARGS(&amp;PSO1)</code>, where <i>PSO1</i> is the name of the object.


### -param ppPipelineState [out]

Type: <b>void**</b>

Specifies a pointer that will reference the returned PSO.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if the name doesn’t exist, or if the input description doesn’t match the data in the library, and E_OUTOFMEMORY if unable to allocate the return PSO. 





## -remarks



Refer to the remarks and examples for <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary">ID3D12PipelineLibrary</a>
 

 

