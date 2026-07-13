---
UID: NN:d3d10sdklayers.ID3D10Debug
title: ID3D10Debug (d3d10sdklayers.h)
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on. (ID3D10Debug)
helpviewer_keywords: ["9243084e-1ae3-39f6-3e6b-d8150af7e0cc","ID3D10Debug","ID3D10Debug interface [Direct3D 10]","ID3D10Debug interface [Direct3D 10]","described","d3d10sdklayers/ID3D10Debug","direct3d10.id3d10debug"]
old-location: direct3d10\id3d10debug.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug.htm
ms.date: 12/05/2018
ms.keywords: 9243084e-1ae3-39f6-3e6b-d8150af7e0cc, ID3D10Debug, ID3D10Debug interface [Direct3D 10], ID3D10Debug interface [Direct3D 10],described, d3d10sdklayers/ID3D10Debug, direct3d10.id3d10debug
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
 - ID3D10Debug
 - d3d10sdklayers/ID3D10Debug
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
 - ID3D10Debug
---

# ID3D10Debug interface


## -description

A debug interface controls debug settings, validates pipeline state and can only be used if the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a> is turned on.

## -inheritance

The <b>ID3D10Debug</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Debug</b> also has these types of members:

## -remarks

This interface is obtained by querying it from the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
