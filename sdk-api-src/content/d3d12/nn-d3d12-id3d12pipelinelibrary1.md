---
UID: NN:d3d12.ID3D12PipelineLibrary1
title: ID3D12PipelineLibrary1 (d3d12.h)
description: Manages a pipeline library. This interface extends ID3D12PipelineLibrary to load PSOs from a pipeline state stream description.
helpviewer_keywords: ["ID3D12PipelineLibrary1","ID3D12PipelineLibrary1 interface","ID3D12PipelineLibrary1 interface","described","d3d12/ID3D12PipelineLibrary1","direct3d12.id3d12pipelinelibrary1"]
old-location: direct3d12\id3d12pipelinelibrary1.htm
tech.root: direct3d12
ms.assetid: 66890F5B-7C1F-4E47-B141-253FC2A166B1
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineLibrary1, ID3D12PipelineLibrary1 interface, ID3D12PipelineLibrary1 interface,described, d3d12/ID3D12PipelineLibrary1, direct3d12.id3d12pipelinelibrary1
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12PipelineLibrary1
 - d3d12/ID3D12PipelineLibrary1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12PipelineLibrary1
---

# ID3D12PipelineLibrary1 interface


## -description

Manages a pipeline library. This interface extends <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary">ID3D12PipelineLibrary</a> to load PSOs from a pipeline state stream description.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12PipelineLibrary1</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary">ID3D12PipelineLibrary</a>. <b>ID3D12PipelineLibrary1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12PipelineLibrary1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary1-loadpipeline">LoadPipeline</a>
</td>
<td align="left" width="63%">
Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database and remembered in order to prevent duplication of PSO contents.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary">ID3D12PipelineLibrary</a>