---
UID: NS:d3d10_1.D3D10_TEXCUBE_ARRAY_SRV1
title: D3D10_TEXCUBE_ARRAY_SRV1
author: windows-sdk-content
description: Specifies the subresource(s) from an array of cube textures to use in a shader-resource view.
old-location: direct3d10\d3d10_texcube_array_srv1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texcube_array_srv1.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 7e56cb00-6357-582e-88ab-2d9d2918ebce, D3D10_TEXCUBE_ARRAY_SRV1, D3D10_TEXCUBE_ARRAY_SRV1 structure [Direct3D 10], d3d10_1/D3D10_TEXCUBE_ARRAY_SRV1, direct3d10.d3d10_texcube_array_srv1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10_1.h
req.include-header: D3D10_1Shader.h
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
req.typenames: D3D10_TEXCUBE_ARRAY_SRV1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1.h
api_name:
 - D3D10_TEXCUBE_ARRAY_SRV1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEXCUBE_ARRAY_SRV1 structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">cube textures</a> to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b>.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of mipmap levels to use.


### -field First2DArrayFace

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first 2D texture to use.


### -field NumCubes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of cube textures in the array.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb694534(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>).

This structure requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

