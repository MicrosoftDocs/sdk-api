---
UID: NF:d3d11.CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT)
title: CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_RASTERIZER_DESC structure that is initialized with default rasterizer-state values.
helpviewer_keywords: ["CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC constructor [Direct3D 11]","CD3D11_RASTERIZER_DESC constructor [Direct3D 11]","CD3D11_RASTERIZER_DESC interface","CD3D11_RASTERIZER_DESC interface [Direct3D 11]","CD3D11_RASTERIZER_DESC constructor","CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT)","CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT)","d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC","direct3d11.cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_"]
old-location: direct3d11\cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_.htm
tech.root: direct3d11
ms.assetid: 6D2B2D68-C3ED-460F-B253-583A1DEF5DAA
ms.date: 12/05/2018
ms.keywords: CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC constructor [Direct3D 11], CD3D11_RASTERIZER_DESC constructor [Direct3D 11],CD3D11_RASTERIZER_DESC interface, CD3D11_RASTERIZER_DESC interface [Direct3D 11],CD3D11_RASTERIZER_DESC constructor, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT), CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT), d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, direct3d11.cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_
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

# CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151654(v=vs.85)">CD3D11_RASTERIZER_DESC</a> structure that is initialized with default rasterizer-state values.

## -parameters

### -param unnamedParam1

Address of the **D3D11_RASTERIZER_DESC** structure that initializes the **CD3D11_RASTERIZER_DESC** structure.

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