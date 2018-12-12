---
UID: NF:d3d11.CD3D11_TEXTURE3D_DESC.CD3D11_TEXTURE3D_DESC(DXGI_FORMAT,UINT,UINT,UINT,UINT,UINT,D3D11_USAGE,UINT,UINT)
title: CD3D11_TEXTURE3D_DESC::CD3D11_TEXTURE3D_DESC(DXGI_FORMAT,UINT,UINT,UINT,UINT,UINT,D3D11_USAGE,UINT,UINT)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_TEXTURE3D_DESC structure that is initialized with D3D11_TEXTURE3D_DESC values.
old-location: direct3d11\cd3d11_texture3d_desc_cd3d11_texture3d_desc_d3d11_texture3d_desc_values_.htm
tech.root: direct3d11
ms.assetid: 4623BE8D-55C9-4CB2-9F0E-40ABE5667EAD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CD3D11_TEXTURE3D_DESC, CD3D11_TEXTURE3D_DESC constructor [Direct3D 11], CD3D11_TEXTURE3D_DESC constructor [Direct3D 11],CD3D11_TEXTURE3D_DESC interface, CD3D11_TEXTURE3D_DESC interface [Direct3D 11],CD3D11_TEXTURE3D_DESC constructor, CD3D11_TEXTURE3D_DESC.CD3D11_TEXTURE3D_DESC, CD3D11_TEXTURE3D_DESC.CD3D11_TEXTURE3D_DESC(DXGI_FORMAT,UINT,UINT,UINT,UINT,UINT,D3D11_USAGE,UINT,UINT), CD3D11_TEXTURE3D_DESC::CD3D11_TEXTURE3D_DESC, CD3D11_TEXTURE3D_DESC::CD3D11_TEXTURE3D_DESC(DXGI_FORMAT,UINT,UINT,UINT,UINT,UINT,D3D11_USAGE,UINT,UINT), d3d11/CD3D11_TEXTURE3D_DESC::CD3D11_TEXTURE3D_DESC, direct3d11.cd3d11_texture3d_desc_cd3d11_texture3d_desc_d3d11_texture3d_desc_values_
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
 - CD3D11_TEXTURE3D_DESC.CD3D11_TEXTURE3D_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D11_TEXTURE3D_DESC::CD3D11_TEXTURE3D_DESC(DXGI_FORMAT,UINT,UINT,UINT,UINT,UINT,D3D11_USAGE,UINT,UINT)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/3C2AE448-2EB1-445C-9885-449E02D79EC3">CD3D11_TEXTURE3D_DESC</a> structure that is initialized with <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a> values.


## -parameters




### -param format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value that specifies the texture format.


### -param width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture width (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device.


### -param height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture height (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device.


### -param depth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture depth (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device.


### -param mipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of mipmap levels in the texture. See the remarks in <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>. Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


### -param bindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies how to bind the texture to pipeline stages.


### -param usage

Type: <b><a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a></b>

A <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>-typed value that identifies how the texture is to be read from and written to.


### -param cpuaccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the types of CPU access allowed.


### -param miscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value identifies other, less common resource options.


## -see-also




<a href="https://msdn.microsoft.com/3C2AE448-2EB1-445C-9885-449E02D79EC3">CD3D11_TEXTURE3D_DESC</a>
 

 

