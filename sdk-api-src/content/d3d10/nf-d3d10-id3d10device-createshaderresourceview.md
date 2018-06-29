---
UID: NF:d3d10.ID3D10Device.CreateShaderResourceView
title: ID3D10Device::CreateShaderResourceView
author: windows-sdk-content
description: Create a shader-resource view for accessing data in a resource.
old-location: direct3d10\id3d10device_createshaderresourceview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createshaderresourceview.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 0714089a-e113-6e43-f46d-91d40fd54005, CreateShaderResourceView, CreateShaderResourceView method [Direct3D 10], CreateShaderResourceView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateShaderResourceView method, ID3D10Device.CreateShaderResourceView, ID3D10Device::CreateShaderResourceView, d3d10/ID3D10Device::CreateShaderResourceView, direct3d10.id3d10device_createshaderresourceview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateShaderResourceView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateShaderResourceView


## -description


Create a shader-resource <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">resource</a> that will serve as input to a shader. This resource must have been created with the <a href="https://msdn.microsoft.com/library/Bb204891(v=VS.85).aspx">D3D10_BIND_SHADER_RESOURCE</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb172437(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC</a>*</b>

Pointer to a shader-resource-view description (see <a href="https://msdn.microsoft.com/library/Bb172437(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).


### -param ppSRView [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A resource is made up of one or more <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">subresources</a>, a view identifies which subresources to allow the pipeline to access. In addition, each resource is bound to the pipeline using a view. A shader-resource view is designed to bind any buffer or texture resource to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">shader stages</a> using the following API methods: <a href="https://msdn.microsoft.com/library/Bb173629(v=VS.85).aspx">VSSetShaderResources</a>, <a href="https://msdn.microsoft.com/library/Bb173583(v=VS.85).aspx">GSSetShaderResources</a> and <a href="https://msdn.microsoft.com/library/Bb173606(v=VS.85).aspx">PSSetShaderResources</a>.

Since a view is fully typed, this means that typeless resources become fully typed when bound to the pipeline.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

