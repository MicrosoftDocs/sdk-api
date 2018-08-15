---
UID: NE:d3d10.D3D10_RESOURCE_DIMENSION
title: D3D10_RESOURCE_DIMENSION
author: windows-sdk-content
description: Identifies the type of resource being used.
old-location: direct3d10\d3d10_resource_dimension.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_resource_dimension.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 63b970df-266a-f05f-9db6-cec5c9ae14a6, D3D10_RESOURCE_DIMENSION, D3D10_RESOURCE_DIMENSION enumeration [Direct3D 10], D3D10_RESOURCE_DIMENSION_BUFFER, D3D10_RESOURCE_DIMENSION_TEXTURE1D, D3D10_RESOURCE_DIMENSION_TEXTURE2D, D3D10_RESOURCE_DIMENSION_TEXTURE3D, D3D10_RESOURCE_DIMENSION_UNKNOWN, d3d10/D3D10_RESOURCE_DIMENSION, d3d10/D3D10_RESOURCE_DIMENSION_BUFFER, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE1D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE2D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE3D, d3d10/D3D10_RESOURCE_DIMENSION_UNKNOWN, direct3d10.d3d10_resource_dimension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
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
req.typenames: D3D10_RESOURCE_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RESOURCE_DIMENSION
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_RESOURCE_DIMENSION enumeration


## -description


Identifies the type of <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">resource</a> being used.


## -enum-fields




### -field D3D10_RESOURCE_DIMENSION_UNKNOWN

Resource is of unknown type.


### -field D3D10_RESOURCE_DIMENSION_BUFFER

Resource is a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE1D

Resource is a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">1D texture</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE2D

Resource is a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE3D

Resource is a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">3D texture</a>.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/en-us/library/Bb173831(v=VS.85).aspx">ID3D10Resource::GetType</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb172695(v=VS.85).aspx">D3DX10_IMAGE_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205275(v=VS.85).aspx">Resource Enumerations</a>
 

 

