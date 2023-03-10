---
UID: NN:d3d11_1.ID3D11RasterizerState1
title: ID3D11RasterizerState1 (d3d11_1.h)
description: The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage. This rasterizer-state interface supports forced sample count.
helpviewer_keywords: ["ID3D11RasterizerState1","ID3D11RasterizerState1 interface [Direct3D 11]","ID3D11RasterizerState1 interface [Direct3D 11]","described","d3d11_1/ID3D11RasterizerState1","direct3d11.id3d11rasterizerstate1"]
old-location: direct3d11\id3d11rasterizerstate1.htm
tech.root: direct3d11
ms.assetid: 771BA97B-1DC4-46DD-AAB6-DFC1100F844D
ms.date: 12/05/2018
ms.keywords: ID3D11RasterizerState1, ID3D11RasterizerState1 interface [Direct3D 11], ID3D11RasterizerState1 interface [Direct3D 11],described, d3d11_1/ID3D11RasterizerState1, direct3d11.id3d11rasterizerstate1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11RasterizerState1
 - d3d11_1/ID3D11RasterizerState1
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
 - ID3D11RasterizerState1
---

# ID3D11RasterizerState1 interface


## -description

The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>. This rasterizer-state interface supports forced sample count.

## -inheritance

The <b>ID3D11RasterizerState1</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>. <b>ID3D11RasterizerState1</b> also has these types of members:

## -remarks

To create a rasterizer-state object, call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1">ID3D11Device1::CreateRasterizerState1</a>. To bind the rasterizer-state object to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">ID3D11DeviceContext::RSSetState</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>
