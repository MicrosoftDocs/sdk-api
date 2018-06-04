---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_RENDER_TARGET_VIEW_DESC structure


## -description


Describes the subresources from a resource that are accessible by using a render-target view.


## -struct-fields




### -field Format

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value that specifies the viewing format.


### -field ViewDimension

A <a href="https://msdn.microsoft.com/16689D46-D5DC-4119-8148-BCFF0E358D6E">D3D12_RTV_DIMENSION</a>-typed value that specifies how the render-target resource will be accessed. This type specifies how the resource will be accessed. This member also determines which _RTV to use in the following union.


### -field Buffer

A <a href="https://msdn.microsoft.com/B4BDA7DE-6FB1-4806-9207-42EA0BFC69AE">D3D12_BUFFER_RTV</a> structure that specifies which buffer elements can be accessed.


### -field Texture1D

A <a href="https://msdn.microsoft.com/F675EC46-C747-4F05-8676-ECB8745F5064">D3D12_TEX1D_RTV</a> structure that specifies the subresources in a 1D texture that can be accessed.


### -field Texture1DArray

A <a href="https://msdn.microsoft.com/AA297BF7-682B-4141-9F5B-D0C3B271C15A">D3D12_TEX1D_ARRAY_RTV</a> structure that specifies the subresources in a 1D texture array that can be accessed.


### -field Texture2D

A <a href="https://msdn.microsoft.com/E85CC5DF-96A9-488E-95A3-60175FA7B63E">D3D12_TEX2D_RTV</a> structure that specifies the subresources in a 2D texture that can be accessed.


### -field Texture2DArray

A <a href="https://msdn.microsoft.com/E20A8045-46A4-40CB-98E9-B148AD2B9BDA">D3D12_TEX2D_ARRAY_RTV</a> structure that specifies the subresources in a 2D texture array that can be accessed.


### -field Texture2DMS

A <a href="https://msdn.microsoft.com/000B37D4-261D-48E1-B7ED-EEA1EC2DA0DD">D3D12_TEX2DMS_RTV</a> structure that specifies a single subresource because a multisampled 2D texture only contains one subresource.


### -field Texture2DMSArray

A <a href="https://msdn.microsoft.com/9EA35677-1680-4F57-BDE1-5649C1D48661">D3D12_TEX2DMS_ARRAY_RTV</a> structure that specifies the subresources in a multisampled 2D texture array that can be accessed.


### -field Texture3D

A <a href="https://msdn.microsoft.com/D640C247-FDE9-49DD-88AB-BCCC3B8880D1">D3D12_TEX3D_RTV</a> structure that specifies subresources in a 3D texture that can be accessed.


## -remarks



Pass a render-target-view description into <a href="https://msdn.microsoft.com/B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4">ID3D12Device::CreateRenderTargetView</a> to create a render-target view.

A render-target view can't use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

