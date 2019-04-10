---
UID: NS:d3d10.D3D10_RENDER_TARGET_VIEW_DESC
title: D3D10_RENDER_TARGET_VIEW_DESC (d3d10.h)
author: windows-sdk-content
description: Specifies the subresource(s) from a resource that are accessible using a render-target view.
old-location: direct3d10\d3d10_render_target_view_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_render_target_view_desc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5e255a6a-0061-9fe8-11d9-e7f4391dd52d, D3D10_RENDER_TARGET_VIEW_DESC, D3D10_RENDER_TARGET_VIEW_DESC structure [Direct3D 10], d3d10/D3D10_RENDER_TARGET_VIEW_DESC, direct3d10.d3d10_render_target_view_desc
ms.topic: struct
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RENDER_TARGET_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_RENDER_TARGET_VIEW_DESC
req.redist: 
---

# D3D10_RENDER_TARGET_VIEW_DESC structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from a resource that are accessible using a render-target view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

The data format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>).


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172414(v=VS.85).aspx">D3D10_RTV_DIMENSION</a></b>

The resource type (see <a href="https://msdn.microsoft.com/en-us/library/Bb172414(v=VS.85).aspx">D3D10_RTV_DIMENSION</a>), which specifies how the render-target resource will be accessed.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204897(v=VS.85).aspx">D3D10_BUFFER_RTV</a></b>

Specifies which buffer elements can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb204897(v=VS.85).aspx">D3D10_BUFFER_RTV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172462(v=VS.85).aspx">D3D10_TEX1D_RTV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172462(v=VS.85).aspx">D3D10_TEX1D_RTV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172459(v=VS.85).aspx">D3D10_TEX1D_ARRAY_RTV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172459(v=VS.85).aspx">D3D10_TEX1D_ARRAY_RTV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172474(v=VS.85).aspx">D3D10_TEX2D_RTV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172474(v=VS.85).aspx">D3D10_TEX2D_RTV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172471(v=VS.85).aspx">D3D10_TEX2D_ARRAY_RTV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172471(v=VS.85).aspx">D3D10_TEX2D_ARRAY_RTV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172468(v=VS.85).aspx">D3D10_TEX2DMS_RTV</a></b>

Specifies a single subresource because a multisampled 2D texture only contains one subresource (see <a href="https://msdn.microsoft.com/en-us/library/Bb172468(v=VS.85).aspx">D3D10_TEX2DMS_RTV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172465(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_RTV</a></b>

Specifies the subresources in a multisampled 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172465(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_RTV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172476(v=VS.85).aspx">D3D10_TEX3D_RTV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="https://msdn.microsoft.com/en-us/library/Bb172476(v=VS.85).aspx">D3D10_TEX3D_RTV</a>).


## -remarks



A render-target-view description is passed into <a href="https://msdn.microsoft.com/en-us/library/Bb173556(v=VS.85).aspx">ID3D10Device::CreateRenderTargetView</a> to create a render target.

A render-target-view cannot use the following formats:

<ul>
<li>Any <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">typeless format</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>, then the format of the resource that the view binds to the pipeline will be used.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

