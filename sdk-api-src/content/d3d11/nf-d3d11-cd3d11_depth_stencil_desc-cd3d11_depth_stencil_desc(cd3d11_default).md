---
UID: NF:d3d11.CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT)
title: CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_DEPTH_STENCIL_DESC structure that is initialized with default depth-stencil-state values.
helpviewer_keywords: ["CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC interface","CD3D11_DEPTH_STENCIL_DESC interface [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC constructor","CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT)","CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT)","d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC","direct3d11.cd3d11_depth_stencil_desc_cd3d11_depth_stencil_desc_cd3d11_default"]
old-location: direct3d11\cd3d11_depth_stencil_desc_cd3d11_depth_stencil_desc_cd3d11_default.htm
tech.root: direct3d11
ms.assetid: 2790BD45-45BB-4BB7-B0B5-07B37ACC2128
ms.date: 12/05/2018
ms.keywords: CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11], CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11],CD3D11_DEPTH_STENCIL_DESC interface, CD3D11_DEPTH_STENCIL_DESC interface [Direct3D 11],CD3D11_DEPTH_STENCIL_DESC constructor, CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT), CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT), d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC, direct3d11.cd3d11_depth_stencil_desc_cd3d11_depth_stencil_desc_cd3d11_default
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
 - CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC
 - d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC
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
 - CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC
---

# CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(CD3D11_DEFAULT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151632(v=vs.85)">CD3D11_DEPTH_STENCIL_DESC</a> structure that is initialized with default depth-stencil-state values.

## -parameters

### -param unnamedParam1

Default depth-stencil-state values.

## -remarks

Here are the default depth-stencil-state values for the members of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>:

```
DepthEnable = TRUE;
        DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
        DepthFunc = D3D11_COMPARISON_LESS;
        StencilEnable = FALSE;
        StencilReadMask = D3D11_DEFAULT_STENCIL_READ_MASK;
        StencilWriteMask = D3D11_DEFAULT_STENCIL_WRITE_MASK;
        const D3D11_DEPTH_STENCILOP_DESC defaultStencilOp =
        { D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_KEEP, D3D11_COMPARISON_ALWAYS };
        FrontFace = defaultStencilOp;
        BackFace = defaultStencilOp;

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151632(v=vs.85)">CD3D11_DEPTH_STENCIL_DESC</a>