---
UID: NN:d3d11sdklayers.ID3D11Debug
title: ID3D11Debug (d3d11sdklayers.h)
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on. (ID3D11Debug)
helpviewer_keywords: ["ID3D11Debug","ID3D11Debug interface [Direct3D 11]","ID3D11Debug interface [Direct3D 11]","described","b037763f-251a-579c-a6cb-8e5097410d05","d3d11sdklayers/ID3D11Debug","direct3d11.id3d11debug"]
old-location: direct3d11\id3d11debug.htm
tech.root: direct3d11
ms.assetid: 2c640295-7a91-4a7a-92d3-909d288eb0d6
ms.date: 12/05/2018
ms.keywords: ID3D11Debug, ID3D11Debug interface [Direct3D 11], ID3D11Debug interface [Direct3D 11],described, b037763f-251a-579c-a6cb-8e5097410d05, d3d11sdklayers/ID3D11Debug, direct3d11.id3d11debug
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
 - ID3D11Debug
 - d3d11sdklayers/ID3D11Debug
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
 - ID3D11Debug
---

# ID3D11Debug interface


## -description

A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.

## -inheritance

The <b>ID3D11Debug</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Debug</b> also has these types of members:

## -remarks

This interface is obtained by querying it from the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.
          

For more information about the debug layer, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
