---
UID: NF:d3d11.ID3D11Device.CreateTexture3D
title: ID3D11Device::CreateTexture3D
author: windows-sdk-content
description: Create a single 3D texture.
old-location: direct3d11\id3d11device_createtexture3d.htm
old-project: direct3d11
ms.assetid: 92b31baf-2d64-47fe-bd0d-550f2a65ed9a
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CreateTexture3D, CreateTexture3D method [Direct3D 11], CreateTexture3D method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateTexture3D method, ID3D11Device.CreateTexture3D, ID3D11Device::CreateTexture3D, d3d11/ID3D11Device::CreateTexture3D, d98ea118-c203-f23f-517e-92225bfe119d, direct3d11.id3d11device_createtexture3d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateTexture3D
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateTexture3D


## -description


Create a single <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">3D texture</a>.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a> structure that describes a 3D texture resource. To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.


### -param pInitialData [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a> structures that describe subresources for the 3D texture resource. Applications cannot specify <b>NULL</b> for <i>pInitialData</i> when creating IMMUTABLE resources (see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>). If the resource is multisampled, <i>pInitialData</i> must be <b>NULL</b> because multisampled resources cannot be initialized with data when they are created.

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the resource is undefined. In this case, you need to write the resource content some other way before the resource is read.

You can determine the size of this array from the value in the <b>MipLevels</b> member of the <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a> structure to which <i>pDesc</i> points. Arrays of 3D volume textures are not supported.

For more information about this array size, see Remarks.


### -param ppTexture3D [out, optional]

Type: <b><a href="https://msdn.microsoft.com/178d4ac4-c71f-40cb-bcaf-45ca96b36350">ID3D11Texture3D</a>**</b>

A pointer to a buffer that receives a pointer to a <a href="https://msdn.microsoft.com/178d4ac4-c71f-40cb-bcaf-45ca96b36350">ID3D11Texture3D</a> interface for the created texture. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for failing error codes.




## -remarks



<b>CreateTexture3D</b> creates a 3D texture resource, which can contain a number of 3D subresources. The number of textures is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more subresources. To load data into the texture, applications can supply the data initially as an array of <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a> structures pointed to by <i>pInitialData</i>, or they can use one of the D3DX texture functions such as <a href="https://msdn.microsoft.com/a84ea166-2296-48d9-a028-b65fd68f2371">D3DX11CreateTextureFromFile</a>.

Each element of <i>pInitialData</i> provides all of the slices that are defined for a given miplevel. For example, for a 32 x 32 x 4 volume texture with a full mipmap chain, the array has the following 6 elements:

<ul>
<li>pInitialData[0] = 32x32 with 4 slices</li>
<li>pInitialData[1] = 16x16 with 2 slices</li>
<li>pInitialData[2] = 8x8 with 1 slice</li>
<li>pInitialData[3] = 4x4
with 1 slice</li>
<li>pInitialData[4] = 2x2
with 1 slice</li>
<li>pInitialData[5] = 1x1
with 1 slice</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

