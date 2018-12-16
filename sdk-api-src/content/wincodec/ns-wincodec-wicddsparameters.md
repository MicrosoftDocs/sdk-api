---
UID: NS:wincodec.WICDdsParameters
title: WICDdsParameters
author: windows-sdk-content
description: Specifies the DDS image dimension, DXGI_FORMAT and alpha mode of contained data.
old-location: wic\wicddsparameters.htm
tech.root: wic
ms.assetid: 2E5755B4-E8DC-40B2-8DA1-B053A261079B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PWICDdsParameters, PWICDdsParameters structure pointer [Windows Imaging Component], WICDdsParameters, WICDdsParameters structure [Windows Imaging Component], wic.wicddsparameters, wincodec/PWICDdsParameters, wincodec/WICDdsParameters
ms.topic: struct
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
 - Wincodec.h
api_name:
 - WICDdsParameters
product: Windows
targetos: Windows
req.typenames: WICDdsParameters
req.redist: 
---

# WICDdsParameters structure


## -description


Specifies the DDS image dimension, <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> and alpha mode of contained data.


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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> of the DDS pixel data.


### -field Dimension

Type: <b><a href="https://msdn.microsoft.com/76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55">WICDdsDimension</a></b>

Specifies the dimension type of the data contained in DDS image (1D, 2D, 3D or cube texture).


### -field AlphaMode

Type: <b><a href="https://msdn.microsoft.com/67C9B07F-5259-4032-9EBF-CBC3B8637343">WICDdsAlphaMode</a></b>

Specifies the alpha behavior of the DDS image.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>



<a href="https://msdn.microsoft.com/67C9B07F-5259-4032-9EBF-CBC3B8637343">WICDdsAlphaMode</a>



<a href="https://msdn.microsoft.com/76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55">WICDdsDimension</a>
 

 

