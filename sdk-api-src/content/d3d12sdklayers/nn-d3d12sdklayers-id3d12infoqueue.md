---
UID: NN:d3d12sdklayers.ID3D12InfoQueue
title: ID3D12InfoQueue (d3d12sdklayers.h)
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack. (ID3D12InfoQueue)
helpviewer_keywords: ["ID3D12InfoQueue","ID3D12InfoQueue interface","ID3D12InfoQueue interface","described","d3d12sdklayers/ID3D12InfoQueue","direct3d12.id3d12infoqueue"]
old-location: direct3d12\id3d12infoqueue.htm
tech.root: direct3d12
ms.assetid: 61667AAC-05AC-4745-8992-E9377641D411
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue, ID3D12InfoQueue interface, ID3D12InfoQueue interface,described, d3d12sdklayers/ID3D12InfoQueue, direct3d12.id3d12infoqueue
req.header: d3d12sdklayers.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12InfoQueue
 - d3d12sdklayers/ID3D12InfoQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue
---

# ID3D12InfoQueue interface


## -description

An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.

## -inheritance

The <b>ID3D12InfoQueue</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12InfoQueue</b> also has these types of members:

## -remarks

This interface is obtained by querying it from the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> using <code>IUnknown::QueryInterface</code>. The <code>ID3D12Debug</code> layer must be enabled through <code>ID3D12Debug::EnableDebugLayer</code> for that operation to succeed.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
