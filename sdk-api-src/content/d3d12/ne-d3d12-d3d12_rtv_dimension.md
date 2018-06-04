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

# D3D12_RTV_DIMENSION enumeration


## -description


Identifies the type of resource to view as a render target.


## -enum-fields




### -field D3D12_RTV_DIMENSION_UNKNOWN

Do not use this value, as it will cause <a href="https://msdn.microsoft.com/B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4">ID3D12Device::CreateRenderTargetView</a> to fail.


### -field D3D12_RTV_DIMENSION_BUFFER

The resource will be accessed as a buffer.


### -field D3D12_RTV_DIMENSION_TEXTURE1D

The resource will be accessed as a 1D texture.


### -field D3D12_RTV_DIMENSION_TEXTURE1DARRAY

The resource will be accessed as an array of 1D textures.


### -field D3D12_RTV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.


### -field D3D12_RTV_DIMENSION_TEXTURE2DARRAY

The resource will be accessed as an array of 2D textures.


### -field D3D12_RTV_DIMENSION_TEXTURE2DMS

The resource will be accessed as a 2D texture with multisampling.


### -field D3D12_RTV_DIMENSION_TEXTURE2DMSARRAY

The resource will be accessed as an array of 2D textures with multisampling.


### -field D3D12_RTV_DIMENSION_TEXTURE3D

The resource will be accessed as a 3D texture.


## -remarks



Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

