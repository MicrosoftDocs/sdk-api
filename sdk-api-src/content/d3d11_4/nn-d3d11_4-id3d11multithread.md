---
UID: NN:d3d11_4.ID3D11Multithread
title: ID3D11Multithread (d3d11_4.h)
description: Provides threading protection for critical sections of a multi-threaded application.
helpviewer_keywords: ["ID3D11Multithread","ID3D11Multithread interface [Direct3D 11]","ID3D11Multithread interface [Direct3D 11]","described","d3d11_4/ID3D11Multithread","direct3d11.id3d11multithread"]
old-location: direct3d11\id3d11multithread.htm
tech.root: direct3d11
ms.assetid: 1A07694E-7D61-4A59-82E3-048F04C8D57A
ms.date: 12/05/2018
ms.keywords: ID3D11Multithread, ID3D11Multithread interface [Direct3D 11], ID3D11Multithread interface [Direct3D 11],described, d3d11_4/ID3D11Multithread, direct3d11.id3d11multithread
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: D3d11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Multithread
 - d3d11_4/ID3D11Multithread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.dll
api_name:
 - ID3D11Multithread
---

# ID3D11Multithread interface


## -description

Provides threading protection for critical sections of a multi-threaded application.

## -inheritance

The <b>ID3D11Multithread</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Multithread</b> also has these types of members:

## -remarks

This interface is obtained by querying it from an immediate device context created with the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> (or later versions of this) interface 
          using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

Unlike D3D10, there is no multithreaded layer in D3D11. By default, multithread protection is turned off. Use <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-setmultithreadprotected">SetMultithreadProtected</a> to turn it on, then <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-enter">Enter</a> and <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-leave">Leave</a> to encapsulate graphics commands that  must be executed in a specific order.

By default in D3D11, applications can only use one thread with the immediate context at a time. But, applications can use this interface to change that restriction. The interface can turn on threading protection for the immediate context, which will increase the overhead of each immediate context call in order to share one context with multiple threads.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
