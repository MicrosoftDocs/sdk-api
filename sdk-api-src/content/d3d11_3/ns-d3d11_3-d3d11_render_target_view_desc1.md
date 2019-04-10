---
UID: NS:d3d11_3.D3D11_RENDER_TARGET_VIEW_DESC1
title: D3D11_RENDER_TARGET_VIEW_DESC1 (d3d11_3.h)
author: windows-sdk-content
description: Describes the subresources from a resource that are accessible using a render-target view.
old-location: direct3d11\d3d11_render_target_view_desc1.htm
tech.root: direct3d11
ms.assetid: D87F06B4-7574-4BBD-A481-653CA35B8FB2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CD3D11_RENDER_TARGET_VIEW_DESC1, D3D11_RENDER_TARGET_VIEW_DESC1, D3D11_RENDER_TARGET_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_RENDER_TARGET_VIEW_DESC1, direct3d11.d3d11_render_target_view_desc1
ms.topic: struct
req.header: d3d11_3.h
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
 - D3D11_3.h
api_name:
 - D3D11_RENDER_TARGET_VIEW_DESC1
product: Windows
targetos: Windows
req.typenames: D3D11_RENDER_TARGET_VIEW_DESC1
req.redist: 
---

# D3D11_RENDER_TARGET_VIEW_DESC1 structure


## -description


Describes the subresources from a resource that are accessible using a render-target view.


## -struct-fields




#### - Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that specifies the data format.




#### - ViewDimension

A <a href="https://msdn.microsoft.com/42cbd3ec-fa8a-48ea-be88-bbe46db13566">D3D11_RTV_DIMENSION</a>-typed value that specifies the resource type and how the render-target resource will be accessed.


#### - Buffer

A <a href="https://msdn.microsoft.com/979c69cf-f9b5-4b10-92ff-ad5245880802">D3D11_BUFFER_RTV</a> structure that specifies which buffer elements can be accessed.


#### - Texture1D

A <a href="https://msdn.microsoft.com/48b32ca3-39c4-437a-a4e5-468c9b52b425">D3D11_TEX1D_RTV</a> structure that specifies the subresources in a 1D texture that can be accessed.


#### - Texture1DArray

A <a href="https://msdn.microsoft.com/cdb1c9e0-39a4-415e-a91f-05042b1f1b2d">D3D11_TEX1D_ARRAY_RTV</a> structure that specifies the subresources in a 1D texture array that can be accessed.


#### - Texture2D

A <a href="https://msdn.microsoft.com/CA815C7D-BA10-4C1B-A6E6-8B42229179B1">D3D11_TEX2D_RTV1</a> structure that specifies the subresources in a 2D texture that can be accessed.


#### - Texture2DArray

A <a href="https://msdn.microsoft.com/AD1C80E6-B2C7-4110-B3C0-6A2B2063198B">D3D11_TEX2D_ARRAY_RTV1</a> structure that specifies the subresources in a 2D texture array that can be accessed.


#### - Texture2DMS

A <a href="https://msdn.microsoft.com/5414183c-4abf-4030-a148-ade5c9213635">D3D11_TEX2DMS_RTV</a> structure that specifies a single subresource because a multisampled 2D texture only contains one subresource.


#### - Texture2DMSArray

A <a href="https://msdn.microsoft.com/ec08341c-980f-4d5f-8eb9-f41835105b46">D3D11_TEX2DMS_ARRAY_RTV</a> structure that specifies the subresources in a multisampled 2D texture array that can be accessed.


#### - Texture3D

A <a href="https://msdn.microsoft.com/58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1">D3D11_TEX3D_RTV</a> structure that specifies subresources in a 3D texture that can be accessed.


## -remarks



A render-target-view description is passed into <a href="https://msdn.microsoft.com/9B85B007-F8B0-43C1-999E-75E5243B7B5A">ID3D11Device3::CreateRenderTargetView1</a> to create a render target.

A render-target-view can't use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

