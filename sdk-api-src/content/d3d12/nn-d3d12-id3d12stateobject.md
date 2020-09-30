---
UID: NN:d3d12.ID3D12StateObject
title: ID3D12StateObject (d3d12.h)
description: Represents a variable amount of configuration state, including shaders, that an application manages as a single unit and which is given to a driver atomically to process, such as compile or optimize.
helpviewer_keywords: ["ID3D12StateObject","ID3D12StateObject interface","ID3D12StateObject interface","described","d3d12/ID3D12StateObject","direct3d12.id3d12stateobject"]
old-location: direct3d12\id3d12stateobject.htm
tech.root: direct3d12
ms.assetid: 5BE94583-31DC-4469-9049-7768D64F7F41
ms.date: 12/05/2018
ms.keywords: ID3D12StateObject, ID3D12StateObject interface, ID3D12StateObject interface,described, d3d12/ID3D12StateObject, direct3d12.id3d12stateobject
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
 - ID3D12StateObject
 - d3d12/ID3D12StateObject
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
 - ID3D12StateObject
---

# ID3D12StateObject interface


## -description

Represents a variable amount of configuration state, including shaders, that an application manages as a single unit and which is given to a driver atomically to process, such as compile or optimize. Create a state object by calling <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject">ID3D12Device5::CreateStateObject</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>