---
UID: NF:d3d12.ID3D12StateObjectProperties.GetPipelineStackSize
title: ID3D12StateObjectProperties::GetPipelineStackSize (d3d12.h)
description: Gets the current pipeline stack size.
helpviewer_keywords: ["GetPipelineStackSize","GetPipelineStackSize method","GetPipelineStackSize method","ID3D12StateObjectProperties interface","ID3D12StateObjectProperties interface","GetPipelineStackSize method","ID3D12StateObjectProperties.GetPipelineStackSize","ID3D12StateObjectProperties::GetPipelineStackSize","d3d12/ID3D12StateObjectProperties::GetPipelineStackSize","direct3d12.id3d12stateobjectproperties_getpipelinestacksize"]
old-location: direct3d12\id3d12stateobjectproperties_getpipelinestacksize.htm
tech.root: direct3d12
ms.assetid: 6570D84B-F589-4090-8F08-F91B12B0E283
ms.date: 12/05/2018
ms.keywords: GetPipelineStackSize, GetPipelineStackSize method, GetPipelineStackSize method,ID3D12StateObjectProperties interface, ID3D12StateObjectProperties interface,GetPipelineStackSize method, ID3D12StateObjectProperties.GetPipelineStackSize, ID3D12StateObjectProperties::GetPipelineStackSize, d3d12/ID3D12StateObjectProperties::GetPipelineStackSize, direct3d12.id3d12stateobjectproperties_getpipelinestacksize
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
 - ID3D12StateObjectProperties::GetPipelineStackSize
 - d3d12/ID3D12StateObjectProperties::GetPipelineStackSize
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
 - ID3D12StateObjectProperties.GetPipelineStackSize
---

# ID3D12StateObjectProperties::GetPipelineStackSize


## -description

Gets the current pipeline stack size.



## -returns

The current pipeline stack size in bytes. When called on non-executable state objects, such as collections, the return value is 0.

## -remarks

This method and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12stateobjectproperties-setpipelinestacksize">SetPipelineStackSize</a> are not re-entrant.  This means if calling either or both from separate threads, the app must synchronize on its own.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12stateobjectproperties.md">ID3D12StateObjectProperties</a>
