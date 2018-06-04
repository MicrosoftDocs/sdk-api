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

# D3D12_SRV_DIMENSION enumeration


## -description


Identifies the type of resource that will be viewed as a shader resource.


## -enum-fields




### -field D3D12_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D12_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D12_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D12_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D12_SRV_DIMENSION_TEXTURECUBEARRAY

The resource is an array of cube textures.


## -remarks



These values are used by a shader-resource-view description, <a href="https://msdn.microsoft.com/2B4B868F-3E9F-4570-B1C7-2767ED717A3B">D3D12_SHADER_RESOURCE_VIEW_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

