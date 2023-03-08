---
UID: NF:d3d12.ID3D12StateObjectProperties.SetPipelineStackSize
title: ID3D12StateObjectProperties::SetPipelineStackSize (d3d12.h)
description: Set the current pipeline stack size.
helpviewer_keywords: ["ID3D12StateObjectProperties interface","SetPipelineStackSize method","ID3D12StateObjectProperties.SetPipelineStackSize","ID3D12StateObjectProperties::SetPipelineStackSize","SetPipelineStackSize","SetPipelineStackSize method","SetPipelineStackSize method","ID3D12StateObjectProperties interface","d3d12/ID3D12StateObjectProperties::SetPipelineStackSize","direct3d12.id3d12stateobjectproperties_setpipelinestacksize"]
old-location: direct3d12\id3d12stateobjectproperties_setpipelinestacksize.htm
tech.root: direct3d12
ms.assetid: 0BB69DBB-F8A1-4C32-AE82-3A49E2E0E4B3
ms.date: 12/05/2018
ms.keywords: ID3D12StateObjectProperties interface,SetPipelineStackSize method, ID3D12StateObjectProperties.SetPipelineStackSize, ID3D12StateObjectProperties::SetPipelineStackSize, SetPipelineStackSize, SetPipelineStackSize method, SetPipelineStackSize method,ID3D12StateObjectProperties interface, d3d12/ID3D12StateObjectProperties::SetPipelineStackSize, direct3d12.id3d12stateobjectproperties_setpipelinestacksize
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
 - ID3D12StateObjectProperties::SetPipelineStackSize
 - d3d12/ID3D12StateObjectProperties::SetPipelineStackSize
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
 - ID3D12StateObjectProperties.SetPipelineStackSize
---

# ID3D12StateObjectProperties::SetPipelineStackSize


## -description

Set the current pipeline stack size.

## -parameters

### -param PipelineStackSizeInBytes

Stack size in bytes to use during pipeline execution for each shader thread. There can be many thousands of threads in flight at once on the GPU.

If the value is greater than 0xffffffff (the maximum value of a 32-bit UINT) the runtime will drop the call, and the debug layer will print an error, as this is likely the result of summing up invalid stack sizes returned from <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12stateobjectproperties-getshaderstacksize">GetShaderStackSize</a> called with invalid parameters, which return 0xffffffff.  In this case, the previously set stack size, or the default, remains.

## -remarks

This method and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12stateobjectproperties-getpipelinestacksize">GetPipelineStackSize</a> are not re-entrant.  This means if calling either or both from separate threads, the app must synchronize on its own.

The runtime drops calls to state objects other than raytracing pipelines, such as collections.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12stateobjectproperties.md">ID3D12StateObjectProperties</a>
