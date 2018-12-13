---
UID: NF:d3d11.CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC(D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT)
title: CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_RENDER_TARGET_VIEW_DESC structure that is initialized with D3D11_RENDER_TARGET_VIEW_DESC values.
old-location: direct3d11\cd3d11_render_target_view_desc_cd3d11_render_target_view_desc_d3d11_render_target_view_desc_values_.htm
tech.root: direct3d11
ms.assetid: 216BB870-029D-4AF2-86EB-F8F11982CA45
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC constructor [Direct3D 11], CD3D11_RENDER_TARGET_VIEW_DESC constructor [Direct3D 11],CD3D11_RENDER_TARGET_VIEW_DESC interface, CD3D11_RENDER_TARGET_VIEW_DESC interface [Direct3D 11],CD3D11_RENDER_TARGET_VIEW_DESC constructor, CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC(D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT), CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC, CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT), d3d11/CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC, direct3d11.cd3d11_render_target_view_desc_cd3d11_render_target_view_desc_d3d11_render_target_view_desc_values_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CD3D11_RENDER_TARGET_VIEW_DESC.CD3D11_RENDER_TARGET_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D11_RENDER_TARGET_VIEW_DESC::CD3D11_RENDER_TARGET_VIEW_DESC(D3D11_RTV_DIMENSION,DXGI_FORMAT,UINT,UINT,UINT)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/28D033EF-3EAC-41F0-A633-D69E4B10343D">CD3D11_RENDER_TARGET_VIEW_DESC</a> structure that is initialized with <a href="https://msdn.microsoft.com/b154ac98-49ed-4d00-8cb6-5e57680e125c">D3D11_RENDER_TARGET_VIEW_DESC</a> values.


## -parameters




### -param viewDimension

Type: <b><a href="https://msdn.microsoft.com/42cbd3ec-fa8a-48ea-be88-bbe46db13566">D3D11_RTV_DIMENSION</a></b>

A <a href="https://msdn.microsoft.com/42cbd3ec-fa8a-48ea-be88-bbe46db13566">D3D11_RTV_DIMENSION</a>-typed value that specifies the resource type of the view.


### -param format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that specifies the viewing format.


### -param mipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the mipmap level to use mip slice. <b>FirstElement</b> for <a href="https://msdn.microsoft.com/2ada8526-bef3-4998-8775-6e062f972a1c">D3D11_BUFFER_SRV</a>.


### -param firstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first element to use in an array of elements.

<b>NumElements</b> for <a href="https://msdn.microsoft.com/2ada8526-bef3-4998-8775-6e062f972a1c">D3D11_BUFFER_SRV</a>. <b>FirstWSlice</b> for <a href="https://msdn.microsoft.com/58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1">D3D11_TEX3D_RTV</a>.


### -param arraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of elements in the array. <b>WSize</b> for <a href="https://msdn.microsoft.com/58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1">D3D11_TEX3D_RTV</a>.


## -see-also




<a href="https://msdn.microsoft.com/28D033EF-3EAC-41F0-A633-D69E4B10343D">CD3D11_RENDER_TARGET_VIEW_DESC</a>
 

 

