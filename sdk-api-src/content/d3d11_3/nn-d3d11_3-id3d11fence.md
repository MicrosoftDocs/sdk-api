---
UID: NN:d3d11_3.ID3D11Fence
title: ID3D11Fence (d3d11_3.h)
description: Represents a fence, an object used for synchronization of the CPU and one or more GPUs. (ID3D11Fence)
helpviewer_keywords: ["ID3D11Fence","ID3D11Fence interface [Direct3D 11]","ID3D11Fence interface [Direct3D 11]","described","d3d11_3/ID3D11Fence","direct3d11.id3d11fence"]
old-location: direct3d11\id3d11fence.htm
tech.root: direct3d11
ms.assetid: DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C
ms.date: 12/05/2018
ms.keywords: ID3D11Fence, ID3D11Fence interface [Direct3D 11], ID3D11Fence interface [Direct3D 11],described, d3d11_3/ID3D11Fence, direct3d11.id3d11fence
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Fence
 - d3d11_3/ID3D11Fence
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11Fence
---

# ID3D11Fence interface


## -description

Represents a fence, an object used for synchronization of the CPU and one or more GPUs.

This interface is equivalent to the Direct3D 12 <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> interface, and is also used for synchronization between Direct3D 11 and Direct3D 12 in interop scenarios.

## -inheritance

The <b>ID3D11Fence</b> interface inherits from <a href="/windows/win32/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11Fence</b> also has these types of members:

## -see-also

<a href="/windows/win32/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/win32/direct3d12/fence-based-resource-management">Fence Based Resource Management (Direct3D 12)</a>



<a href="/windows/win32/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

