---
UID: NF:d3d12.ID3D12PipelineLibrary1.LoadPipeline
title: ID3D12PipelineLibrary1::LoadPipeline
author: windows-sdk-content
description: Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database and remembered in order to prevent duplication of PSO contents.
old-location: direct3d12\id3d12pipelinelibrary1_loadpipeline.htm
old-project: direct3d12
ms.assetid: 842092FF-906D-4595-8C43-07F0349CA1A3
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12PipelineLibrary1 interface,LoadPipeline method, ID3D12PipelineLibrary1.LoadPipeline, ID3D12PipelineLibrary1::LoadPipeline, LoadPipeline, LoadPipeline method, LoadPipeline method,ID3D12PipelineLibrary1 interface, d3d12/ID3D12PipelineLibrary1::LoadPipeline, direct3d12.id3d12pipelinelibrary1_loadpipeline
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
 - ID3D12PipelineLibrary1.LoadPipeline
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12PipelineLibrary1::LoadPipeline


## -description


Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database and remembered in order to prevent duplication of PSO contents.


## -parameters




### -param pName [in]

Type: <b>LPCWSTR</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_</code>

The unique name of the PSO.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a>*</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_</code>

Describes the required PSO using a <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a> structure. This description is matched against the library database and stored in order to prevent duplication of PSO contents.


### -param riid

Type: <b>REFIID</b>

Specifies a REFIID for the ID3D12PipelineStateState object.

Applications should typically set this argument and the following argument, ppPipelineState, by using the macro IID_PPV_ARGS(&amp;PSO1), where PSO1 is the name of the object.


### -param ppPipelineState [out]

Type: <b>void**</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_COM_Outptr_</code>

Specifies the pointer that will reference the PSO after the function successfully returns.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if the name doesn't exist or the stream description doesn't match the data in the library, and E_OUTOFMEMORY if the function is unable to allocate the resulting PSO.




## -remarks



This function takes the pipeline description as a <a href="https://msdn.microsoft.com/2CC9051B-09B1-49F5-9392-3E0AE3AB1277">D3D12_PIPELINE_STATE_STREAM_DESC</a> and is a replacement for the <a href="https://msdn.microsoft.com/1DDD1348-2039-4BF4-9ED8-7AA087D0B654">ID3D12PipelineLibrary::LoadGraphicsPipeline</a> and <a href="https://msdn.microsoft.com/8295D6E3-8353-46AD-A741-170244495F8B">ID3D12PipelineLibrary::LoadComputePipeline</a> functions, which take their pipeline description as the less-flexible <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structs, respectively.




## -see-also




<a href="https://msdn.microsoft.com/66890F5B-7C1F-4E47-B141-253FC2A166B1">ID3D12PipelineLibrary1</a>
 

 

