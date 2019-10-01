---
UID: NN:d3d12.ID3D12PipelineLibrary
title: ID3D12PipelineLibrary (d3d12.h)
author: windows-sdk-content
description: Manages a pipeline library, in particular loading and retrieving individual PSOs.
old-location: direct3d12\id3d12pipelinelibrary.htm
tech.root: direct3d12
ms.assetid: 7A1D750D-51F1-48F6-9D74-6439A147F1EC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineLibrary, ID3D12PipelineLibrary interface, ID3D12PipelineLibrary interface,described, d3d12/ID3D12PipelineLibrary, direct3d12.id3d12pipelinelibrary
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12PipelineLibrary"
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
 - ID3D12PipelineLibrary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12PipelineLibrary interface


## -description


Manages a pipeline library, in particular loading and retrieving individual PSOs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12PipelineLibrary</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>. <b>ID3D12PipelineLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12PipelineLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-getserializedsize">GetSerializedSize</a>
</td>
<td align="left" width="63%">
Returns the amount of memory required to serialize the current contents of the database. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline">LoadComputePipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline">LoadGraphicsPipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-storepipeline">StorePipeline</a>
</td>
<td align="left" width="63%">
Adds the input PSO to an internal database with the corresponding name.

</td>
</tr>
</table> 


## -remarks



Refer to the remarks and examples for <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
 

 

