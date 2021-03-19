---
UID: NF:d3d11.CD3D11_BLEND_DESC.CD3D11_BLEND_DESC(CD3D11_DEFAULT)
title: CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(CD3D11_DEFAULT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_BLEND_DESC structure that is initialized with default blend-state values.
helpviewer_keywords: ["CD3D11_BLEND_DESC","CD3D11_BLEND_DESC constructor [Direct3D 11]","CD3D11_BLEND_DESC constructor [Direct3D 11]","CD3D11_BLEND_DESC interface","CD3D11_BLEND_DESC interface [Direct3D 11]","CD3D11_BLEND_DESC constructor","CD3D11_BLEND_DESC.CD3D11_BLEND_DESC","CD3D11_BLEND_DESC.CD3D11_BLEND_DESC(CD3D11_DEFAULT)","CD3D11_BLEND_DESC::CD3D11_BLEND_DESC","CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(CD3D11_DEFAULT)","d3d11/CD3D11_BLEND_DESC::CD3D11_BLEND_DESC","direct3d11.cd3d11_blend_desc_cd3d11_blend_desc_cd3d11_default_"]
old-location: direct3d11\cd3d11_blend_desc_cd3d11_blend_desc_cd3d11_default_.htm
tech.root: direct3d11
ms.assetid: F1756CCA-463F-48BC-99A2-8E956DDC8A3D
ms.date: 12/05/2018
ms.keywords: CD3D11_BLEND_DESC, CD3D11_BLEND_DESC constructor [Direct3D 11], CD3D11_BLEND_DESC constructor [Direct3D 11],CD3D11_BLEND_DESC interface, CD3D11_BLEND_DESC interface [Direct3D 11],CD3D11_BLEND_DESC constructor, CD3D11_BLEND_DESC.CD3D11_BLEND_DESC, CD3D11_BLEND_DESC.CD3D11_BLEND_DESC(CD3D11_DEFAULT), CD3D11_BLEND_DESC::CD3D11_BLEND_DESC, CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(CD3D11_DEFAULT), d3d11/CD3D11_BLEND_DESC::CD3D11_BLEND_DESC, direct3d11.cd3d11_blend_desc_cd3d11_blend_desc_cd3d11_default_
req.header: d3d11.h
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
 - CD3D11_BLEND_DESC::CD3D11_BLEND_DESC
 - d3d11/CD3D11_BLEND_DESC::CD3D11_BLEND_DESC
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
 - CD3D11_BLEND_DESC.CD3D11_BLEND_DESC
---

# CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(CD3D11_DEFAULT)


## -description

Instantiates a new instance of a <a href="/windows/desktop/api/d3d11/ns-d3d11-cd3d11_blend_desc">CD3D11_BLEND_DESC</a> structure that is initialized with default blend-state values.

## -parameters

### -param unnamedParam1

TBD

## -remarks

Here are the default depth-stencil-state values for the members of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">D3D11_BLEND_DESC</a>:


```
AlphaToCoverageEnable = FALSE;
        IndependentBlendEnable = FALSE;
        const D3D11_RENDER_TARGET_BLEND_DESC defaultRenderTargetBlendDesc =
        {
            FALSE,
            D3D11_BLEND_ONE, D3D11_BLEND_ZERO, D3D11_BLEND_OP_ADD,
            D3D11_BLEND_ONE, D3D11_BLEND_ZERO, D3D11_BLEND_OP_ADD,
            D3D11_COLOR_WRITE_ENABLE_ALL,
        };
        for (UINT i = 0; i < D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT; ++i)
            RenderTarget[ i ] = defaultRenderTargetBlendDesc;

```

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-cd3d11_blend_desc">CD3D11_BLEND_DESC</a>