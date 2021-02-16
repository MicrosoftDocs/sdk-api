---
UID: NF:d3d11.CD3D11_VIEWPORT.CD3D11_VIEWPORT(ID3D11Texture2D,ID3D11RenderTargetView,FLOAT,FLOAT,FLOAT,FLOAT)
title: CD3D11_VIEWPORT::CD3D11_VIEWPORT(ID3D11Texture2D,ID3D11RenderTargetView,FLOAT,FLOAT,FLOAT,FLOAT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_VIEWPORT structure that is initialized with 2D texture values.
helpviewer_keywords: ["CD3D11_VIEWPORT","CD3D11_VIEWPORT interface [Direct3D 11]","CD3D11_VIEWPORT method","CD3D11_VIEWPORT method [Direct3D 11]","CD3D11_VIEWPORT method [Direct3D 11]","CD3D11_VIEWPORT interface","CD3D11_VIEWPORT.CD3D11_VIEWPORT","CD3D11_VIEWPORT.CD3D11_VIEWPORT(ID3D11Texture2D","ID3D11RenderTargetView","FLOAT","FLOAT","FLOAT","FLOAT)","CD3D11_VIEWPORT::CD3D11_VIEWPORT","CD3D11_VIEWPORT::CD3D11_VIEWPORT(ID3D11Texture2D","ID3D11RenderTargetView","FLOAT","FLOAT","FLOAT","FLOAT)","CD3D11_VIEWPORT::CD3D11_VIEWPORT(const D3D11_VIEWPORT&)","d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT","direct3d11.cd3d11_viewport_cd3d11_viewport_d3d11_viewport_"]
old-location: 
tech.root: direct3d11
ms.assetid: F65883C8-C1CA-4A5C-9E74-F6193D53C09F
ms.date: 05/06/2019
ms.keywords: CD3D11_VIEWPORT, CD3D11_VIEWPORT interface [Direct3D 11],CD3D11_VIEWPORT method, CD3D11_VIEWPORT method [Direct3D 11], CD3D11_VIEWPORT method [Direct3D 11],CD3D11_VIEWPORT interface, CD3D11_VIEWPORT.CD3D11_VIEWPORT, CD3D11_VIEWPORT.CD3D11_VIEWPORT(ID3D11Texture2D,ID3D11RenderTargetView,FLOAT,FLOAT,FLOAT,FLOAT), CD3D11_VIEWPORT::CD3D11_VIEWPORT, CD3D11_VIEWPORT::CD3D11_VIEWPORT(ID3D11Texture2D,ID3D11RenderTargetView,FLOAT,FLOAT,FLOAT,FLOAT), CD3D11_VIEWPORT::CD3D11_VIEWPORT(const D3D11_VIEWPORT&), d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT, direct3d11.cd3d11_viewport_cd3d11_viewport_d3d11_viewport_
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
 - CD3D11_VIEWPORT::CD3D11_VIEWPORT
 - d3d11/CD3D11_VIEWPORT::CD3D11_VIEWPORT
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
 - CD3D11_VIEWPORT.CD3D11_VIEWPORT
---

# CD3D11_VIEWPORT::CD3D11_VIEWPORT(ID3D11Texture2D,ID3D11RenderTargetView,FLOAT,FLOAT,FLOAT,FLOAT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151722(v=vs.85)">CD3D11_VIEWPORT</a> structure that is initialized with 2D texture values.

## -parameters

### -param pTex2D

A pointer to a **ID3D11Texture2D** interface for a 2D texture.

### -param pRTView

A pointer to a **ID3D11RenderTargetView** interface for the render-target view.

### -param topLeftX

X position of the left hand side of the viewport.
Ranges between **D3D11_VIEWPORT_BOUNDS_MIN** and **D3D11_VIEWPORT_BOUNDS_MAX**.

### -param topLeftY

Y position of the top of the viewport.
Ranges between **D3D11_VIEWPORT_BOUNDS_MIN** and **D3D11_VIEWPORT_BOUNDS_MAX**.

### -param minDepth

Minimum depth of the viewport.
Ranges between 0 and 1.

### -param maxDepth

Maximum depth of the viewport.
Ranges between 0 and 1.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151722(v=vs.85)">CD3D11_VIEWPORT</a>