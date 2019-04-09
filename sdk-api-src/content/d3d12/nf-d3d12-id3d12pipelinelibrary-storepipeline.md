---
UID: NF:d3d12.ID3D12PipelineLibrary.StorePipeline
title: ID3D12PipelineLibrary::StorePipeline (d3d12.h)
author: windows-sdk-content
description: Adds the input PSO to an internal database with the corresponding name.
old-location: direct3d12\id3d12pipelinelibrary_storepipeline.htm
tech.root: direct3d12
ms.assetid: A7847966-4B31-47EA-A5CB-B6576CD2501F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineLibrary interface,StorePipeline method, ID3D12PipelineLibrary.StorePipeline, ID3D12PipelineLibrary::StorePipeline, StorePipeline, StorePipeline method, StorePipeline method,ID3D12PipelineLibrary interface, d3d12/ID3D12PipelineLibrary::StorePipeline, direct3d12.id3d12pipelinelibrary_storepipeline
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
 - ID3D12PipelineLibrary.StorePipeline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12PipelineLibrary::StorePipeline


## -description


Adds the input PSO to an internal database with the corresponding name.


## -parameters




### -param pName [in, optional]

Type: <b>LPCWSTR</b>

Specifies a unique name for the library. Overwriting is not supported.


### -param pPipeline [in]

Type: <b>ID3D12PipelineState*</b>

Specifies the <a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a> to add.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the name already exists, E_OUTOFMEMORY if unable to allocate storage in the library. 





## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a>
 

 

