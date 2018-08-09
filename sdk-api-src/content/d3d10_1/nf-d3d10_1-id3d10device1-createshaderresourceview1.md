---
UID: NF:d3d10_1.ID3D10Device1.CreateShaderResourceView1
title: ID3D10Device1::CreateShaderResourceView1
author: windows-sdk-content
description: Create a shader-resource view for accessing data in a resource.
old-location: direct3d10\id3d10device1_createshaderresourceview1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1_createshaderresourceview1.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 03e028ae-86fb-9c0c-3e9c-3a0471355fab, CreateShaderResourceView1, CreateShaderResourceView1 method [Direct3D 10], CreateShaderResourceView1 method [Direct3D 10],ID3D10Device1 interface, ID3D10Device1 interface [Direct3D 10],CreateShaderResourceView1 method, ID3D10Device1.CreateShaderResourceView1, ID3D10Device1::CreateShaderResourceView1, d3d10_1/ID3D10Device1::CreateShaderResourceView1, direct3d10.id3d10device1_createshaderresourceview1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10_1.h
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
req.typenames: D3D10_FEATURE_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1.h
api_name:
 - ID3D10Device1.CreateShaderResourceView1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Device1::CreateShaderResourceView1


## -description


Create a shader-resource <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">resource</a> that will serve as input to a shader. This resource must have been created with the <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_SHADER_RESOURCE</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb694534(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>*</b>

Pointer to a shader-resource-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb694534(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>). Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).


### -param ppSRView [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb694557(v=VS.85).aspx">ID3D10ShaderResourceView1</a>**</b>

Address of a pointer to a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb694557(v=VS.85).aspx">ID3D10ShaderResourceView1 Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A resource is made up of one or more <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresources</a>, a view identifies which subresources to allow the pipeline to access. In addition, each resource is bound to the pipeline using a view. A shader-resource view is designed to bind any buffer or texture resource to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">shader stages</a> using the following API methods: <a href="https://msdn.microsoft.com/en-us/library/Bb173629(v=VS.85).aspx">VSSetShaderResources</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb173583(v=VS.85).aspx">GSSetShaderResources</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb173606(v=VS.85).aspx">PSSetShaderResources</a>.

Since a view is fully typed, this means that typeless resources become fully typed when bound to the pipeline.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1 Interface</a>
 

 

