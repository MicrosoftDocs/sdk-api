---
UID: NN:d3d12.ID3D12Device2
title: ID3D12Device2 (d3d12.h)
description: Represents a virtual adapter. This interface extends ID3D12Device1 to create pipeline state objects from pipeline state stream descriptions.
helpviewer_keywords: ["ID3D12Device2","ID3D12Device2 interface","ID3D12Device2 interface","described","d3d12/ID3D12Device2","direct3d12.id3d12device2"]
old-location: direct3d12\id3d12device2.htm
tech.root: direct3d12
ms.assetid: 86C46FD2-7B1D-4F66-97F7-45F9428C5E1E
ms.date: 12/05/2018
ms.keywords: ID3D12Device2, ID3D12Device2 interface, ID3D12Device2 interface,described, d3d12/ID3D12Device2, direct3d12.id3d12device2
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
 - ID3D12Device2
 - d3d12/ID3D12Device2
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
 - ID3D12Device2
---

# ID3D12Device2 interface


## -description

Represents a virtual adapter. This interface extends <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a> to create pipeline state objects from pipeline state stream descriptions.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10 Creators Update. Applications targeting Windows 10 Creators Update should use this interface instead of earlier or later versions. Applications targeting an earlier or later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface.</div><div> </div>

## -inheritance

The <b>ID3D12Device2</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>. <b>ID3D12Device2</b> also has these types of members:

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice">D3D12CreateDevice</a> to create a device.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>
