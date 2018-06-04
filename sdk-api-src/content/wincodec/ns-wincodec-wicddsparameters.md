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

# WICDdsParameters structure


## -description


Specifies the DDS image dimension, <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> and alpha mode of contained data.


## -struct-fields




### -field Width

Type: <b>UINT</b>

The width, in pixels, of the texture at the largest mip size (mip level 0).


### -field Height

Type: <b>UINT</b>

The height, in pixels, of the texture at the largest mip size (mip level 0). When the DDS image contains a 1-dimensional texture, this value is equal to 1.


### -field Depth

Type: <b>UINT</b>

The number of slices in the 3D texture. This is equivalent to the depth, in pixels, of the 3D texture at the largest mip size (mip level 0). When the DDS image contains a 1- or 2-dimensional texture, this value is equal to 1.


### -field MipLevels

Type: <b>UINT</b>

The number of mip levels contained in the DDS image.


### -field ArraySize

Type: <b>UINT</b>

The number of textures in the array in the DDS image.


### -field DxgiFormat

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> of the DDS pixel data.


### -field Dimension

Type: <b><a href="https://msdn.microsoft.com/76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55">WICDdsDimension</a></b>

Specifies the dimension type of the data contained in DDS image (1D, 2D, 3D or cube texture).


### -field AlphaMode

Type: <b><a href="https://msdn.microsoft.com/67C9B07F-5259-4032-9EBF-CBC3B8637343">WICDdsAlphaMode</a></b>

Specifies the alpha behavior of the DDS image.


## -see-also




<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>



<a href="https://msdn.microsoft.com/67C9B07F-5259-4032-9EBF-CBC3B8637343">WICDdsAlphaMode</a>



<a href="https://msdn.microsoft.com/76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55">WICDdsDimension</a>
 

 

