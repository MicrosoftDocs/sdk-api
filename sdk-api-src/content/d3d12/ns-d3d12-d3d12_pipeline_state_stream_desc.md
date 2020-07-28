---
UID: NS:d3d12.D3D12_PIPELINE_STATE_STREAM_DESC
title: D3D12_PIPELINE_STATE_STREAM_DESC (d3d12.h)
description: Describes a pipeline state stream.
helpviewer_keywords: ["D3D12_PIPELINE_STATE_STREAM_DESC","D3D12_PIPELINE_STATE_STREAM_DESC structure","d3d12/D3D12_PIPELINE_STATE_STREAM_DESC","direct3d12.d3d12_pipeline_state_stream_desc"]
old-location: direct3d12\d3d12_pipeline_state_stream_desc.htm
tech.root: direct3d12
ms.assetid: 2CC9051B-09B1-49F5-9392-3E0AE3AB1277
ms.date: 12/05/2018
ms.keywords: D3D12_PIPELINE_STATE_STREAM_DESC, D3D12_PIPELINE_STATE_STREAM_DESC structure, d3d12/D3D12_PIPELINE_STATE_STREAM_DESC, direct3d12.d3d12_pipeline_state_stream_desc
f1_keywords:
- d3d12/D3D12_PIPELINE_STATE_STREAM_DESC
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d12.h
api_name:
- D3D12_PIPELINE_STATE_STREAM_DESC
targetos: Windows
req.typenames: D3D12_PIPELINE_STATE_STREAM_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_PIPELINE_STATE_STREAM_DESC structure


## -description


Describes a pipeline state stream.


## -struct-fields




### -field SizeInBytes

<a href="https://docs.microsoft.com/visualstudio/code-quality/annotating-structs-and-classes?view=vs-2015">SAL</a>: <code>_In_</code>

Specifies the size of the opaque data structure pointed to by the pPipelineStateSubobjectStream member, in bytes.


### -field pPipelineStateSubobjectStream

<a href="https://docs.microsoft.com/visualstudio/code-quality/annotating-structs-and-classes?view=vs-2015">SAL</a>: <code>_In_reads_(_Inexpressible_("Dependentonsizeofsubobjects"))</code>

Specifies the address of a data structure that describes as a bytestream an arbitrary pipeline state subobject.


## -remarks



Use this structure with the ID3D12Device1::CreatePipelineState method to create pipeline state objects.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

