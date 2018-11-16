---
UID: NN:d3d12.ID3D12PipelineLibrary
title: ID3D12PipelineLibrary
author: windows-sdk-content
description: Manages a pipeline library, in particular loading and retrieving individual PSOs.
old-location: direct3d12\id3d12pipelinelibrary.htm
tech.root: direct3d12
ms.assetid: 7A1D750D-51F1-48F6-9D74-6439A147F1EC
ms.author: windowssdkdev
ms.date: 11/15/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12PipelineLibrary</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn788651(v=VS.85).aspx">ID3D12DeviceChild</a>. <b>ID3D12PipelineLibrary</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Mt709146(v=VS.85).aspx">GetSerializedSize</a>
</td>
<td align="left" width="63%">
Returns the amount of memory required to serialize the current contents of the database. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt709147(v=VS.85).aspx">LoadComputePipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt709148(v=VS.85).aspx">LoadGraphicsPipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt709149(v=VS.85).aspx">Serialize</a>
</td>
<td align="left" width="63%">
Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt709150(v=VS.85).aspx">StorePipeline</a>
</td>
<td align="left" width="63%">
Adds the input PSO to an internal database with the corresponding name.

</td>
</tr>
</table> 


## -remarks



Refer to the remarks and examples for <a href="https://msdn.microsoft.com/en-us/library/Mt709133(v=VS.85).aspx">CreatePipelineLibrary</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770457(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn788651(v=VS.85).aspx">ID3D12DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709473(v=VS.85).aspx">Root Signature Version 1.1</a>
 

 

