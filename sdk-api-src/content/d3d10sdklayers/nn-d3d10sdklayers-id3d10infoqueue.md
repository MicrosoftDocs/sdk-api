---
UID: NN:d3d10sdklayers.ID3D10InfoQueue
title: ID3D10InfoQueue (d3d10sdklayers.h)
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack. (ID3D10InfoQueue)
helpviewer_keywords: ["1ef0bd38-23d3-fa53-cf27-ff502bb674f2","ID3D10InfoQueue","ID3D10InfoQueue interface [Direct3D 10]","ID3D10InfoQueue interface [Direct3D 10]","described","d3d10sdklayers/ID3D10InfoQueue","direct3d10.id3d10infoqueue"]
old-location: direct3d10\id3d10infoqueue.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue.htm
ms.date: 12/05/2018
ms.keywords: 1ef0bd38-23d3-fa53-cf27-ff502bb674f2, ID3D10InfoQueue, ID3D10InfoQueue interface [Direct3D 10], ID3D10InfoQueue interface [Direct3D 10],described, d3d10sdklayers/ID3D10InfoQueue, direct3d10.id3d10infoqueue
req.header: d3d10sdklayers.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10InfoQueue
 - d3d10sdklayers/ID3D10InfoQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10InfoQueue
---

# ID3D10InfoQueue interface


## -description

An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.

## -inheritance

The <b>ID3D10InfoQueue</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10InfoQueue</b> also has these types of members:

## -remarks

This interface is obtained by turning on the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a> and querying it from the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.


```
hr = D3D10CreateDeviceAndSwapChain( NULL, g_driverType, NULL, D3D10_CREATE_DEVICE_DEBUG, D3D10_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3dDevice );
...
ID3D10InfoQueue * infoQueue;
g_pd3dDevice->QueryInterface(__uuidof(ID3D10InfoQueue),  (void **)&infoQueue); 

```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
