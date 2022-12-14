---
UID: NF:d3d12.ID3D12GraphicsCommandList4.DispatchRays
title: ID3D12GraphicsCommandList4::DispatchRays (d3d12.h)
description: Launch the threads of a ray generation shader.
helpviewer_keywords: ["DispatchRays","DispatchRays method","DispatchRays method","ID3D12GraphicsCommandList4 interface","ID3D12GraphicsCommandList4 interface","DispatchRays method","ID3D12GraphicsCommandList4.DispatchRays","ID3D12GraphicsCommandList4::DispatchRays","d3d12/ID3D12GraphicsCommandList4::DispatchRays","direct3d12.id3d12graphicscommandlist4_dispatchrays"]
old-location: direct3d12\id3d12graphicscommandlist4_dispatchrays.htm
tech.root: direct3d12
ms.assetid: 157F4609-B9AF-40EC-A2E6-33D5A897A813
ms.date: 12/05/2018
ms.keywords: DispatchRays, DispatchRays method, DispatchRays method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,DispatchRays method, ID3D12GraphicsCommandList4.DispatchRays, ID3D12GraphicsCommandList4::DispatchRays, d3d12/ID3D12GraphicsCommandList4::DispatchRays, direct3d12.id3d12graphicscommandlist4_dispatchrays
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - ID3D12GraphicsCommandList4::DispatchRays
 - d3d12/ID3D12GraphicsCommandList4::DispatchRays
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
 - ID3D12GraphicsCommandList4.DispatchRays
---

# ID3D12GraphicsCommandList4::DispatchRays


## -description

Launch the threads of a ray generation shader.

## -parameters

### -param pDesc [in]

A description of the ray dispatch

## -remarks

This method can be called from graphics or compute command lists and bundles.



A raytracing pipeline state must be set on the command list. Otherwise, the behavior of this call is undefined.

There are 3 dimensions passed in to set the grid size:  width/height/depth.  These dimensions are constrained such that width * height * depth &lt;= 2^30. Exceeding this produces undefined behavior. 
If any grid dimension is 0, no threads are launched.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>

