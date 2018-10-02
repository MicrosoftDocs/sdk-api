---
UID: NE:d3d11.D3D11_RESOURCE_DIMENSION
title: D3D11_RESOURCE_DIMENSION
author: windows-sdk-content
description: Identifies the type of resource being used.
old-location: direct3d11\d3d11_resource_dimension.htm
tech.root: direct3d11
ms.assetid: 56f138a2-9f2b-4f3b-8619-d9f394704b8a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 6d57af93-82b7-a916-56c4-587636f7f9c4, D3D11_RESOURCE_DIMENSION, D3D11_RESOURCE_DIMENSION enumeration [Direct3D 11], D3D11_RESOURCE_DIMENSION_BUFFER, D3D11_RESOURCE_DIMENSION_TEXTURE1D, D3D11_RESOURCE_DIMENSION_TEXTURE2D, D3D11_RESOURCE_DIMENSION_TEXTURE3D, D3D11_RESOURCE_DIMENSION_UNKNOWN, d3d11/D3D11_RESOURCE_DIMENSION, d3d11/D3D11_RESOURCE_DIMENSION_BUFFER, d3d11/D3D11_RESOURCE_DIMENSION_TEXTURE1D, d3d11/D3D11_RESOURCE_DIMENSION_TEXTURE2D, d3d11/D3D11_RESOURCE_DIMENSION_TEXTURE3D, d3d11/D3D11_RESOURCE_DIMENSION_UNKNOWN, direct3d11.d3d11_resource_dimension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_RESOURCE_DIMENSION
product: Windows
targetos: Windows
req.typenames: D3D11_RESOURCE_DIMENSION
req.redist: 
---

# D3D11_RESOURCE_DIMENSION enumeration


## -description


Identifies the type of resource being used.


## -enum-fields




### -field D3D11_RESOURCE_DIMENSION_UNKNOWN

Resource is of unknown type.


### -field D3D11_RESOURCE_DIMENSION_BUFFER

Resource is a buffer.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE1D

Resource is a 1D texture.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE2D

Resource is a 2D texture.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE3D

Resource is a 3D texture.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/en-us/library/Ff476586(v=VS.85).aspx">ID3D11Resource::GetType</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476170(v=VS.85).aspx">Resource Enumerations</a>
 

 

