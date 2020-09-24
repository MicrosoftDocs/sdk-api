---
UID: NF:d3d11.CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT)
title: CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT) (d3d11.h)
description: Instantiates a new instance of a CD3D11_DEPTH_STENCIL_VIEW_DESC structure that is initialized with D3D11_DEPTH_STENCIL_VIEW_DESC values.
helpviewer_keywords: ["CD3D11_DEPTH_STENCIL_VIEW_DESC","CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_VIEW_DESC interface","CD3D11_DEPTH_STENCIL_VIEW_DESC interface [Direct3D 11]","CD3D11_DEPTH_STENCIL_VIEW_DESC constructor","CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC","CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION","DXGI_FORMAT","UINT","UINT","UINT","UINT)","CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC","CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION","DXGI_FORMAT","UINT","UINT","UINT","UINT)","d3d11/CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC","direct3d11.cd3d11_depth_stencil_view_desc_cd3d11_depth_stencil_view_desc_d3d11_depth_stencil_view_desc_values_"]
old-location: direct3d11\cd3d11_depth_stencil_view_desc_cd3d11_depth_stencil_view_desc_d3d11_depth_stencil_view_desc_values_.htm
tech.root: direct3d11
ms.assetid: 6E45B810-D92F-47A1-A102-10D60BBC02F3
ms.date: 12/05/2018
ms.keywords: CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11], CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11],CD3D11_DEPTH_STENCIL_VIEW_DESC interface, CD3D11_DEPTH_STENCIL_VIEW_DESC interface [Direct3D 11],CD3D11_DEPTH_STENCIL_VIEW_DESC constructor, CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT), CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT), d3d11/CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC, direct3d11.cd3d11_depth_stencil_view_desc_cd3d11_depth_stencil_view_desc_d3d11_depth_stencil_view_desc_values_
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
 - CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC
 - d3d11/CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC
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
 - CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC
---

# CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT)


## -description

Instantiates a new instance of a <a href="/previous-versions/windows/desktop/legacy/jj151639(v=vs.85)">CD3D11_DEPTH_STENCIL_VIEW_DESC</a> structure that is initialized with <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a> values.

## -parameters

### -param viewDimension

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_dsv_dimension">D3D11_DSV_DIMENSION</a></b>

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_dsv_dimension">D3D11_DSV_DIMENSION</a>-typed value that specifies the depth-stencil type of the view.

### -param format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the viewing format.

### -param mipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use mip slice.

### -param firstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first element to use in an array of elements.

### -param arraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of elements in the array.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that describes whether the texture is read only.  Pass 0 to specify that it is not read only; otherwise, pass one of the members of 
        the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_dsv_flag">D3D11_DSV_FLAG</a> enumerated type.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj151639(v=vs.85)">CD3D11_DEPTH_STENCIL_VIEW_DESC</a>