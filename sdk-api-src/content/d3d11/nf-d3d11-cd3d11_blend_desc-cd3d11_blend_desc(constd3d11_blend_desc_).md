---
UID: NF:d3d11.CD3D11_BLEND_DESC.CD3D11_BLEND_DESC(const D3D11_BLEND_DESC &)
title: CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(const D3D11_BLEND_DESC &)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_BLEND_DESC structure that is initialized with default blend-state values.
old-location: direct3d11\cd3d11_blend_desc_cd3d11_blend_desc_cd3d11_default_.htm
tech.root: direct3d11
ms.assetid: F1756CCA-463F-48BC-99A2-8E956DDC8A3D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CD3D11_BLEND_DESC, CD3D11_BLEND_DESC constructor [Direct3D 11], CD3D11_BLEND_DESC constructor [Direct3D 11],CD3D11_BLEND_DESC interface, CD3D11_BLEND_DESC interface [Direct3D 11],CD3D11_BLEND_DESC constructor, CD3D11_BLEND_DESC.CD3D11_BLEND_DESC, CD3D11_BLEND_DESC.CD3D11_BLEND_DESC(const D3D11_BLEND_DESC &), CD3D11_BLEND_DESC::CD3D11_BLEND_DESC, CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(CD3D11_DEFAULT), CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(const D3D11_BLEND_DESC &), d3d11/CD3D11_BLEND_DESC::CD3D11_BLEND_DESC, direct3d11.cd3d11_blend_desc_cd3d11_blend_desc_cd3d11_default_
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D11_BLEND_DESC::CD3D11_BLEND_DESC(const D3D11_BLEND_DESC &)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/EC45CD9E-FD2E-4D1D-9D35-1CD7C5B8085D">CD3D11_BLEND_DESC</a> structure that is initialized with default blend-state values.


## -parameters




### -param o

TBD






## -remarks



Here are the default depth-stencil-state values for the members of <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a>:


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




<a href="https://msdn.microsoft.com/EC45CD9E-FD2E-4D1D-9D35-1CD7C5B8085D">CD3D11_BLEND_DESC</a>
 

 

