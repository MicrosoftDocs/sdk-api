---
UID: NF:d3d12.ID3D12PipelineLibrary.LoadGraphicsPipeline
title: ID3D12PipelineLibrary::LoadGraphicsPipeline
author: windows-sdk-content
description: Retrieves the requested PSO from the library.
old-location: direct3d12\id3d12pipelinelibrary_loadgraphicspipeline.htm
tech.root: direct3d12
ms.assetid: 1DDD1348-2039-4BF4-9ED8-7AA087D0B654
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12PipelineLibrary interface,LoadGraphicsPipeline method, ID3D12PipelineLibrary.LoadGraphicsPipeline, ID3D12PipelineLibrary::LoadGraphicsPipeline, LoadGraphicsPipeline, LoadGraphicsPipeline method, LoadGraphicsPipeline method,ID3D12PipelineLibrary interface, d3d12/ID3D12PipelineLibrary::LoadGraphicsPipeline, direct3d12.id3d12pipelinelibrary_loadgraphicspipeline
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
 - ID3D12PipelineLibrary.LoadGraphicsPipeline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12PipelineLibrary.LoadGraphicsPipeline
: 
---

# ID3D12PipelineLibrary::LoadGraphicsPipeline


## -description


Retrieves the requested PSO from the library. 


## -parameters




### -param pName [in]

Type: <b>LPCWSTR</b>

The unique name of the PSO.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a>*</b>

Specifies a description of the required PSO in a <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure. This input description is matched against the data in the current library database, and stored in order to prevent duplication of PSO contents.


### -param riid

Type: <b>REFIID</b>

Specifies a REFIID for the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> object. Typically set this, and the following parameter, with the macro <code>IID_PPV_ARGS(&amp;PSO1)</code>, where <i>PSO1</i> is the name of the object.


### -param ppPipelineState [out]

Type: <b>void**</b>

Specifies a pointer that will reference the returned PSO.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if the name doesn’t exist, or if the input description doesn’t match the data in the library, and E_OUTOFMEMORY if unable to allocate the return PSO. 





## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a>
 

 

