---
UID: NN:d3d11shadertracing.ID3D11ShaderTraceFactory
title: ID3D11ShaderTraceFactory (d3d11shadertracing.h)
description: An ID3D11ShaderTraceFactory interface implements a method for generating shader trace information objects.
helpviewer_keywords: ["ID3D11ShaderTraceFactory","ID3D11ShaderTraceFactory interface [Direct3D 11]","ID3D11ShaderTraceFactory interface [Direct3D 11]","described","d3d11shadertracing/ID3D11ShaderTraceFactory","direct3d11.id3d11shadertracefactory"]
old-location: direct3d11\id3d11shadertracefactory.htm
tech.root: direct3d11
ms.assetid: 0B90EA4B-0176-49DC-8A57-4D847552EFA3
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderTraceFactory, ID3D11ShaderTraceFactory interface [Direct3D 11], ID3D11ShaderTraceFactory interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTraceFactory, direct3d11.id3d11shadertracefactory
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: D3D11SDKLayers.dll; D3D11_1SDKLayers.dll; D3D11_2SDKLayers.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderTraceFactory
 - d3d11shadertracing/ID3D11ShaderTraceFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11SDKLayers.dll
 - D3D11_1SDKLayers.dll
 - D3D11_2SDKLayers.dll
api_name:
 - ID3D11ShaderTraceFactory
---

# ID3D11ShaderTraceFactory interface


## -description

An <b>ID3D11ShaderTraceFactory</b> interface implements a method for generating shader trace information objects.

## -inheritance

The <b>ID3D11ShaderTraceFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderTraceFactory</b> also has these types of members:

## -remarks

These APIs require the Windows Software Development Kit (SDK) for Windows 8.

To retrieve an instance of <b>ID3D11ShaderTraceFactory</b>, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> that you created with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_DEBUGGABLE</a>.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
