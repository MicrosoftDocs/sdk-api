---
UID: NF:d3d11.CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D,D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT)
title: CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D,D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_RENDER_TARGET_VIEW_DESC structure that is initialized with 2D texture  values.
helpviewer_keywords: ["CD3D11_RENDER_TARGET_VIEW_DESC","CD3D11_RENDER_TARGET_VIEW_DESC interface [Direct3D 11]","CD3D11_RENDER_TARGET_VIEW_DESC method","CD3D11_RENDER_TARGET_VIEW_DESC method [Direct3D 11]","CD3D11_RENDER_TARGET_VIEW_DESC method [Direct3D 11]","CD3D11_RENDER_TARGET_VIEW_DESC interface","CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC","CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D","D3D11_RTV_DIMENSION","DXGI_FORMAT","UINT","UINT","UINT)","CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC","CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D","D3D11_RTV_DIMENSION","DXGI_FORMAT","UINT","UINT","UINT)","CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(const D3D11_RENDER_TARGET_VIEW_DESC&)","d3d11/CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC","direct3d11.cd3d11_render_target_view_desc_cd3d11_render_target_view_desc_d3d11_render_target_view_desc_"]
old-location: 
tech.root: direct3d11
ms.assetid: 7CF6FD80-4DCA-4090-8BB0-384BDA0B4856
ms.date: 05/06/2019
ms.keywords: CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC interface [Direct3D 11],CD3D11_RENDER_TARGET_VIEW_DESC method, CD3D11_RENDER_TARGET_VIEW_DESC method [Direct3D 11], CD3D11_RENDER_TARGET_VIEW_DESC method [Direct3D 11],CD3D11_RENDER_TARGET_VIEW_DESC interface, CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D,D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT), CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D,D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT), CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(const D3D11_RENDER_TARGET_VIEW_DESC&), d3d11/CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC, direct3d11.cd3d11_render_target_view_desc_cd3d11_render_target_view_desc_d3d11_render_target_view_desc_
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
 - CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC
 - d3d11/CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC
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
 - CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC
---

# CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(ID3D11Texture2D,D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151668(v=vs.85)">CD3D11_RENDER_TARGET_VIEW_DESC</a> structure that is initialized with 2D texture  values.

## -parameters

### -param pTex2D

A pointer to a **ID3D11Texture2D** interface for a 2D texture.

### -param viewDimension

A **D3D11_RTV_DIMENSION**-typed value that specifies the resource type of the view.

### -param format

A DXGI_FORMAT-typed value that specifies the viewing format.

### -param mipSlice

The index of the mipmap level to use mip slice.

### -param firstArraySlice

The index of the first element to use in an array of elements.

### -param arraySize

Number of elements in the array.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151668(v=vs.85)">CD3D11_RENDER_TARGET_VIEW_DESC</a>