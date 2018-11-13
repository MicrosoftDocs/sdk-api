---
UID: NS:d3d10.D3D10_RENDER_TARGET_VIEW_DESC
title: D3D10_RENDER_TARGET_VIEW_DESC
author: windows-sdk-content
description: Specifies the subresource(s) from a resource that are accessible using a render-target view.
old-location: direct3d10\d3d10_render_target_view_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_render_target_view_desc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 5e255a6a-0061-9fe8-11d9-e7f4391dd52d, D3D10_RENDER_TARGET_VIEW_DESC, D3D10_RENDER_TARGET_VIEW_DESC structure [Direct3D 10], d3d10/D3D10_RENDER_TARGET_VIEW_DESC, direct3d10.d3d10_render_target_view_desc
ms.prod: windows
ms.technology: windows-sdk
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


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource(s)</a> from a resource that are accessible using a render-target view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The data format (see <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>).


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/233b7954-80ef-4de7-a0d6-a9290a8b0e33">D3D10_RTV_DIMENSION</a></b>

The resource type (see <a href="https://msdn.microsoft.com/233b7954-80ef-4de7-a0d6-a9290a8b0e33">D3D10_RTV_DIMENSION</a>), which specifies how the render-target resource will be accessed.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/24f56262-a6df-464a-ad5e-dc0252807548">D3D10_BUFFER_RTV</a></b>

Specifies which buffer elements can be accessed (see <a href="https://msdn.microsoft.com/24f56262-a6df-464a-ad5e-dc0252807548">D3D10_BUFFER_RTV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/11f5b38a-76f0-41a5-b9fe-7eb15bc09fa9">D3D10_TEX1D_RTV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="https://msdn.microsoft.com/11f5b38a-76f0-41a5-b9fe-7eb15bc09fa9">D3D10_TEX1D_RTV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/3e738535-32d0-4f29-a569-4095b01e7f53">D3D10_TEX1D_ARRAY_RTV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="https://msdn.microsoft.com/3e738535-32d0-4f29-a569-4095b01e7f53">D3D10_TEX1D_ARRAY_RTV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/7c53f1b4-1f81-453d-8fe9-41f022ac87ec">D3D10_TEX2D_RTV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="https://msdn.microsoft.com/7c53f1b4-1f81-453d-8fe9-41f022ac87ec">D3D10_TEX2D_RTV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/f17b4810-1c72-4992-a754-02fa3dc55573">D3D10_TEX2D_ARRAY_RTV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/f17b4810-1c72-4992-a754-02fa3dc55573">D3D10_TEX2D_ARRAY_RTV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/458b8bed-42c3-45c5-96c7-fd7cb3964f6d">D3D10_TEX2DMS_RTV</a></b>

Specifies a single subresource because a multisampled 2D texture only contains one subresource (see <a href="https://msdn.microsoft.com/458b8bed-42c3-45c5-96c7-fd7cb3964f6d">D3D10_TEX2DMS_RTV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/e74aa10f-8f5b-4551-83a4-9a8861a2edf8">D3D10_TEX2DMS_ARRAY_RTV</a></b>

Specifies the subresources in a multisampled 2D texture array that can be accessed (see <a href="https://msdn.microsoft.com/e74aa10f-8f5b-4551-83a4-9a8861a2edf8">D3D10_TEX2DMS_ARRAY_RTV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/5cad08ef-8a97-4ba5-98d5-25ef301aaa94">D3D10_TEX3D_RTV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="https://msdn.microsoft.com/5cad08ef-8a97-4ba5-98d5-25ef301aaa94">D3D10_TEX3D_RTV</a>).


## -remarks



A render-target-view description is passed into <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a> to create a render target.

A render-target-view cannot use the following formats:

<ul>
<li>Any <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">typeless format</a>.</li>
<li>
<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>, then the format of the resource that the view binds to the pipeline will be used.




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

