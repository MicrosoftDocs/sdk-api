---
UID: NN:d3d12.ID3D12Pageable
title: ID3D12Pageable (d3d12.h)
description: An interface from which many other core interfaces inherit from. It indicates that the object type encapsulates some amount of GPU-accessible memory; but does not strongly indicate whether the application can manipulate the object's residency.
helpviewer_keywords: ["ID3D12Pageable","ID3D12Pageable interface","ID3D12Pageable interface","described","d3d12/ID3D12Pageable","direct3d12.id3d12pageable"]
old-location: direct3d12\id3d12pageable.htm
tech.root: direct3d12
ms.assetid: 89DC88B4-9DFD-413D-8EB9-91087CC90D18
ms.date: 12/05/2018
ms.keywords: ID3D12Pageable, ID3D12Pageable interface, ID3D12Pageable interface,described, d3d12/ID3D12Pageable, direct3d12.id3d12pageable
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
 - ID3D12Pageable
 - d3d12/ID3D12Pageable
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
 - ID3D12Pageable
---

# ID3D12Pageable interface


## -description

An interface from which many other core interfaces inherit from. It indicates that the object type encapsulates some amount of GPU-accessible memory; but does not strongly indicate whether the application can manipulate the object's residency.

## -remarks

For more details, refer to <a href="/windows/desktop/direct3d12/memory-management">Memory Management in Direct3D 12</a> and the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-makeresident">MakeResident</a> method reference.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/direct3d12/creating-descriptor-heaps">Creating Descriptor Heaps</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>