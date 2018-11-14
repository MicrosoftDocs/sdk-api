---
UID: NN:d3d12.ID3D12PipelineLibrary
title: ID3D12PipelineLibrary
author: windows-sdk-content
description: Manages a pipeline library, in particular loading and retrieving individual PSOs.
old-location: direct3d12\id3d12pipelinelibrary.htm
tech.root: direct3d12
ms.assetid: 7A1D750D-51F1-48F6-9D74-6439A147F1EC
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12PipelineLibrary, ID3D12PipelineLibrary interface, ID3D12PipelineLibrary interface,described, d3d12/ID3D12PipelineLibrary, direct3d12.id3d12pipelinelibrary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12PipelineLibrary interface


## -description


Manages a pipeline library, in particular loading and retrieving individual PSOs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12PipelineLibrary</b> interface inherits from <a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>. <b>ID3D12PipelineLibrary</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/45DA092B-AB9B-43BE-8F5C-AE05485EA3C1">GetSerializedSize</a>
</td>
<td align="left" width="63%">
Returns the amount of memory required to serialize the current contents of the database. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8295D6E3-8353-46AD-A741-170244495F8B">LoadComputePipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1DDD1348-2039-4BF4-9ED8-7AA087D0B654">LoadGraphicsPipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD81B464-1E93-47CF-9D95-8F8F64C39CD6">Serialize</a>
</td>
<td align="left" width="63%">
Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A7847966-4B31-47EA-A5CB-B6576CD2501F">StorePipeline</a>
</td>
<td align="left" width="63%">
Adds the input PSO to an internal database with the corresponding name.

</td>
</tr>
</table> 


## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/572A95A6-A02F-4512-9BDE-2A8CA58A0A27">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

