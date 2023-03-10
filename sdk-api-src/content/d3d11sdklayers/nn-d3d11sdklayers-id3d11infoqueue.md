---
UID: NN:d3d11sdklayers.ID3D11InfoQueue
title: ID3D11InfoQueue (d3d11sdklayers.h)
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack. (ID3D11InfoQueue)
helpviewer_keywords: ["ID3D11InfoQueue","ID3D11InfoQueue interface [Direct3D 11]","ID3D11InfoQueue interface [Direct3D 11]","described","c949addb-3970-af5d-6963-d7a298716036","d3d11sdklayers/ID3D11InfoQueue","direct3d11.id3d11infoqueue"]
old-location: direct3d11\id3d11infoqueue.htm
tech.root: direct3d11
ms.assetid: 240820c7-1c1f-4e2d-8b3e-497fd931d7d2
ms.date: 12/05/2018
ms.keywords: ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], ID3D11InfoQueue interface [Direct3D 11],described, c949addb-3970-af5d-6963-d7a298716036, d3d11sdklayers/ID3D11InfoQueue, direct3d11.id3d11infoqueue
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue
 - d3d11sdklayers/ID3D11InfoQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue
---

# ID3D11InfoQueue interface


## -description

An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.

## -inheritance

The <b>ID3D11InfoQueue</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11InfoQueue</b> also has these types of members:

## -remarks

To get this interface, turn on debug layer and use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> from the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
