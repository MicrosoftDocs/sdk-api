---
UID: NN:d3d10.ID3D10Multithread
title: ID3D10Multithread (d3d10.h)
description: A multithread interface accesses multithread settings and can only be used if the thread-safe layer is turned on.
helpviewer_keywords: ["03af3cb4-f8ff-e677-80ea-33ee09667866","ID3D10Multithread","ID3D10Multithread interface [Direct3D 10]","ID3D10Multithread interface [Direct3D 10]","described","d3d10/ID3D10Multithread","direct3d10.id3d10multithread"]
old-location: direct3d10\id3d10multithread.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread.htm
ms.date: 12/05/2018
ms.keywords: 03af3cb4-f8ff-e677-80ea-33ee09667866, ID3D10Multithread, ID3D10Multithread interface [Direct3D 10], ID3D10Multithread interface [Direct3D 10],described, d3d10/ID3D10Multithread, direct3d10.id3d10multithread
req.header: d3d10.h
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
 - ID3D10Multithread
 - d3d10/ID3D10Multithread
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
 - ID3D10Multithread
---

# ID3D10Multithread interface


## -description

A multithread interface accesses multithread settings and can only be used if the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">thread-safe layer</a> is turned on.

## -inheritance

The <b>ID3D10Multithread</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Multithread</b> also has these types of members:

## -remarks

This interface is obtained by querying it from the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
