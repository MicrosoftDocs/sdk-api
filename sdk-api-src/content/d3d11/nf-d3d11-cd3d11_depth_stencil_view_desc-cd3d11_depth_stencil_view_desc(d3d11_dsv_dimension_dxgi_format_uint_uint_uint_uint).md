---
UID: NF:d3d11.CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT)
title: CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT) (d3d11.h)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_DEPTH_STENCIL_VIEW_DESC structure that is initialized with D3D11_DEPTH_STENCIL_VIEW_DESC values.
old-location: direct3d11\cd3d11_depth_stencil_view_desc_cd3d11_depth_stencil_view_desc_d3d11_depth_stencil_view_desc_values_.htm
tech.root: direct3d11
ms.assetid: 6E45B810-D92F-47A1-A102-10D60BBC02F3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11], CD3D11_DEPTH_STENCIL_VIEW_DESC constructor [Direct3D 11],CD3D11_DEPTH_STENCIL_VIEW_DESC interface, CD3D11_DEPTH_STENCIL_VIEW_DESC interface [Direct3D 11],CD3D11_DEPTH_STENCIL_VIEW_DESC constructor, CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT), CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC, CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT), d3d11/CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC, direct3d11.cd3d11_depth_stencil_view_desc_cd3d11_depth_stencil_view_desc_d3d11_depth_stencil_view_desc_values_
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
 - CD3D11_DEPTH_STENCIL_VIEW_DESC.CD3D11_DEPTH_STENCIL_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D11_DEPTH_STENCIL_VIEW_DESC::CD3D11_DEPTH_STENCIL_VIEW_DESC(D3D11_DSV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT,UINT)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/4DD04DF8-75C3-430C-9AFA-E3344B053D6E">CD3D11_DEPTH_STENCIL_VIEW_DESC</a> structure that is initialized with <a href="https://msdn.microsoft.com/f073a798-edd5-4e6a-a8a7-1592721ce35d">D3D11_DEPTH_STENCIL_VIEW_DESC</a> values.


## -parameters




### -param viewDimension

Type: <b><a href="https://msdn.microsoft.com/3037e940-6915-4b1d-b0ae-cd440033ac38">D3D11_DSV_DIMENSION</a></b>

A <a href="https://msdn.microsoft.com/3037e940-6915-4b1d-b0ae-cd440033ac38">D3D11_DSV_DIMENSION</a>-typed value that specifies the depth-stencil type of the view.


### -param format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that specifies the viewing format.


### -param mipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the mipmap level to use mip slice.


### -param firstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first element to use in an array of elements.


### -param arraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of elements in the array.


### -param flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that describes whether the texture is read only.  Pass 0 to specify that it is not read only; otherwise, pass one of the members of 
        the <a href="https://msdn.microsoft.com/8894ec55-9d56-4d41-a5d6-72ce064e3351">D3D11_DSV_FLAG</a> enumerated type.


## -see-also




<a href="https://msdn.microsoft.com/4DD04DF8-75C3-430C-9AFA-E3344B053D6E">CD3D11_DEPTH_STENCIL_VIEW_DESC</a>
 

 

