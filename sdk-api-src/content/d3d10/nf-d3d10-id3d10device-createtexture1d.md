---
UID: NF:d3d10.ID3D10Device.CreateTexture1D
title: ID3D10Device::CreateTexture1D
author: windows-sdk-content
description: Create an array of 1D textures (see Texture1D).
old-location: direct3d10\id3d10device_createtexture1d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createtexture1d.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 0ea074c9-00a2-6fa9-2aad-24c30631a07a, CreateTexture1D, CreateTexture1D method [Direct3D 10], CreateTexture1D method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateTexture1D method, ID3D10Device.CreateTexture1D, ID3D10Device::CreateTexture1D, d3d10/ID3D10Device::CreateTexture1D, direct3d10.id3d10device_createtexture1d
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
 - ID3D10Device.CreateTexture1D
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateTexture1D


## -description


Create an array of 1D textures (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Texture1D</a>).


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a>*</b>

Pointer to a 1D texture description (see <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a>). To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.


### -param pInitialData [in]

Type: <b>const <a href="https://msdn.microsoft.com/083d9027-5c4d-47f4-9d42-b1016628b210">D3D10_SUBRESOURCE_DATA</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> descriptions (see <a href="https://msdn.microsoft.com/083d9027-5c4d-47f4-9d42-b1016628b210">D3D10_SUBRESOURCE_DATA</a>); one for each subresource (ordered by texture array index). Applications may not specify <b>NULL</b> for pInitialData when creating IMMUTABLE resources (see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a>). If the resource is multisampled, pInitialData must be <b>NULL</b> because multisampled resources cannot be initialized with data when they are created.


### -param ppTexture1D [out]

Type: <b><a href="https://msdn.microsoft.com/d73cdd85-d6e2-4724-a069-6a4edb5b354e">ID3D10Texture1D</a>**</b>

Address of a pointer to the created texture (see <a href="https://msdn.microsoft.com/d73cdd85-d6e2-4724-a069-6a4edb5b354e">ID3D10Texture1D Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a> for failing error codes.




## -remarks



CreateTexture1D creates a 1D texture resource, which contains an array of 1D textures. The number of textures is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a>. To load data into the texture, applications may supply the data initially as part of <a href="https://msdn.microsoft.com/083d9027-5c4d-47f4-9d42-b1016628b210">D3D10_SUBRESOURCE_DATA</a> structure pointed to by pInitialData, or it may use one of the <a href="https://msdn.microsoft.com/6a4945ee-bd82-4c29-9e75-c0e2e5fc1524">Texturing Functions</a> supplied by the SDK.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

