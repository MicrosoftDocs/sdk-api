---
UID: NF:d3d11.CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(constD3D11_RASTERIZER_DESC&)
title: CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &) (d3d11.h)
description: Instantiates a new instance of a CD3D11_RASTERIZER_DESC structure that is initialized with a D3D11_RASTERIZER_DESC structure.
helpviewer_keywords: ["CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC constructor [Direct3D 11]","CD3D11_RASTERIZER_DESC constructor [Direct3D 11]","CD3D11_RASTERIZER_DESC interface","CD3D11_RASTERIZER_DESC interface [Direct3D 11]","CD3D11_RASTERIZER_DESC constructor","CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)","CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT)","CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)","d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC","direct3d11.cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_"]
old-location: 
tech.root: direct3d11
ms.assetid: E0079C8B-C6B7-4EBD-885B-9982527CF04A
ms.date: 05/06/2019
ms.keywords: CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC constructor [Direct3D 11], CD3D11_RASTERIZER_DESC constructor [Direct3D 11],CD3D11_RASTERIZER_DESC interface, CD3D11_RASTERIZER_DESC interface [Direct3D 11],CD3D11_RASTERIZER_DESC constructor, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &), CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT), CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &), d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, direct3d11.cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_
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
 - CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC
 - d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC
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
 - CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC
---

# CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151654(v=vs.85)">CD3D11_RASTERIZER_DESC</a>  structure that is initialized with a **D3D11_RASTERIZER_DESC** structure.

## -parameters

### -param o

Address of the **D3D11_RASTERIZER_DESC** structure that initializes the **D3D11_RASTERIZER_DESC** structure.

## -remarks

Here are the default rasterizer-state values for the members of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>:

```
FillMode = D3D11_FILL_SOLID;
        CullMode = D3D11_CULL_BACK;
        FrontCounterClockwise = FALSE;
        DepthBias = D3D11_DEFAULT_DEPTH_BIAS;
        DepthBiasClamp = D3D11_DEFAULT_DEPTH_BIAS_CLAMP;
        SlopeScaledDepthBias = D3D11_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;
        DepthClipEnable = TRUE;
        ScissorEnable = FALSE;
        MultisampleEnable = FALSE;
        AntialiasedLineEnable = FALSE;

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151654(v=vs.85)">CD3D11_RASTERIZER_DESC</a>