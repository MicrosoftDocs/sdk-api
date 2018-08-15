---
UID: NF:d3d11.ID3D11Device.CreateTexture2D
title: ID3D11Device::CreateTexture2D
author: windows-sdk-content
description: Create an array of 2D textures.
old-location: direct3d11\id3d11device_createtexture2d.htm
old-project: direct3d11
ms.assetid: 69950ce7-9c8e-4f00-860d-e118e2bbc81a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 96e5176c-4fd3-2bab-29e2-e913ad58fe8b, CreateTexture2D, CreateTexture2D method [Direct3D 11], CreateTexture2D method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateTexture2D method, ID3D11Device.CreateTexture2D, ID3D11Device::CreateTexture2D, d3d11/ID3D11Device::CreateTexture2D, direct3d11.id3d11device_createtexture2d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
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
 - ID3D11Device.CreateTexture2D
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateTexture2D


## -description


Create an array of <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">2D textures</a>.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a> structure that describes a 2D texture resource. To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.


### -param pInitialData [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a>*</b>

 A pointer to an array of <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a> structures that describe subresources for the 2D texture resource. Applications can't specify <b>NULL</b> for <i>pInitialData</i> when creating IMMUTABLE resources (see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>). If the resource is multisampled, <i>pInitialData</i> must be <b>NULL</b> because multisampled resources cannot be initialized with data when they are created.

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the resource is undefined. In this case, you need to write the resource content some other way before the resource is read.

You can determine the size of this array from values in the <b>MipLevels</b> and <b>ArraySize</b> members of the <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a> structure to which <i>pDesc</i> points by using the following calculation:

MipLevels * ArraySize

For more information about this array size, see Remarks.


### -param ppTexture2D [out, optional]

Type: <b><a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>**</b>

A pointer to a buffer that receives a pointer to a <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a> interface for the created texture. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for failing error codes.




## -remarks



<b>CreateTexture2D</b> creates a 2D texture resource, which can contain a number of 2D subresources. The number of textures is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more subresources. To load data into the texture, applications can supply the data initially as an array of <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a> structures pointed to by <i>pInitialData</i>, or it may use one of the D3DX texture functions such as <a href="https://msdn.microsoft.com/a84ea166-2296-48d9-a028-b65fd68f2371">D3DX11CreateTextureFromFile</a>.

For a 32 x 32 texture with a full mipmap chain, the <i>pInitialData</i> array has the following 6 elements:


<ul>
<li>pInitialData[0] = 32x32</li>
<li>pInitialData[1] = 16x16</li>
<li>pInitialData[2] = 8x8</li>
<li>pInitialData[3] = 4x4
</li>
<li>pInitialData[4] = 2x2
</li>
<li>pInitialData[5] = 1x1
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

