---
UID: NS:d3d11.D3D11_RENDER_TARGET_VIEW_DESC
title: D3D11_RENDER_TARGET_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresources from a resource that are accessible using a render-target view.
old-location: direct3d11\d3d11_render_target_view_desc.htm
old-project: direct3d11
ms.assetid: b154ac98-49ed-4d00-8cb6-5e57680e125c
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 0571f2fa-1f94-b9a4-ea30-5f99a077c507, D3D11_RENDER_TARGET_VIEW_DESC, D3D11_RENDER_TARGET_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_RENDER_TARGET_VIEW_DESC, direct3d11.d3d11_render_target_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_RENDER_TARGET_VIEW_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_RENDER_TARGET_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_RENDER_TARGET_VIEW_DESC structure


## -description


Specifies the subresources from a resource that are accessible using a render-target view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The data format (see <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>).


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/42cbd3ec-fa8a-48ea-be88-bbe46db13566">D3D11_RTV_DIMENSION</a></b>

The resource type (see <a href="https://msdn.microsoft.com/42cbd3ec-fa8a-48ea-be88-bbe46db13566">D3D11_RTV_DIMENSION</a>), which specifies how the render-target resource will be accessed.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/979c69cf-f9b5-4b10-92ff-ad5245880802">D3D11_BUFFER_RTV</a></b>

Specifies which buffer elements can be accessed (see <a href="https://msdn.microsoft.com/979c69cf-f9b5-4b10-92ff-ad5245880802">D3D11_BUFFER_RTV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/48b32ca3-39c4-437a-a4e5-468c9b52b425">D3D11_TEX1D_RTV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="https://msdn.microsoft.com/48b32ca3-39c4-437a-a4e5-468c9b52b425">D3D11_TEX1D_RTV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/cdb1c9e0-39a4-415e-a91f-05042b1f1b2d">D3D11_TEX1D_ARRAY_RTV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="https://msdn.microsoft.com/cdb1c9e0-39a4-415e-a91f-05042b1f1b2d">D3D11_TEX1D_ARRAY_RTV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/e0f24576-0767-461d-8dc3-b8822ea89fef">D3D11_TEX2D_RTV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="https://msdn.microsoft.com/e0f24576-0767-461d-8dc3-b8822ea89fef">D3D11_TEX2D_RTV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/5caecf26-707b-45f4-8296-784ed4184459">D3D11_TEX2D_ARRAY_RTV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/5caecf26-707b-45f4-8296-784ed4184459">D3D11_TEX2D_ARRAY_RTV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/5414183c-4abf-4030-a148-ade5c9213635">D3D11_TEX2DMS_RTV</a></b>

Specifies a single subresource because a multisampled 2D texture only contains one subresource (see <a href="https://msdn.microsoft.com/5414183c-4abf-4030-a148-ade5c9213635">D3D11_TEX2DMS_RTV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/ec08341c-980f-4d5f-8eb9-f41835105b46">D3D11_TEX2DMS_ARRAY_RTV</a></b>

Specifies the subresources in a multisampled 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/ec08341c-980f-4d5f-8eb9-f41835105b46">D3D11_TEX2DMS_ARRAY_RTV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1">D3D11_TEX3D_RTV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="https://msdn.microsoft.com/58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1">D3D11_TEX3D_RTV</a>).


## -remarks



A render-target-view description is passed into <a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">ID3D11Device::CreateRenderTargetView</a> to create a render target.

A render-target-view cannot use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

