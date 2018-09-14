---
UID: NF:d3d11.D3D11CalcSubresource
title: D3D11CalcSubresource function
author: windows-sdk-content
description: Calculates a subresource index for a texture.
old-location: direct3d11\d3d11calcsubresource.htm
tech.root: direct3d11
ms.assetid: 643a21f7-3c2e-4d62-9236-051f51d31241
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: D3D11CalcSubresource, D3D11CalcSubresource function [Direct3D 11], d3d11/D3D11CalcSubresource, direct3d11.d3d11calcsubresource, ea6ecdec-c3d4-b87d-c8d6-c356afacd091
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.dll: D3d11.lib
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d11.lib
api_name:
 - D3D11CalcSubresource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D11CalcSubresource function


## -description


Calculates a subresource index for a texture.


## -parameters




### -param MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.
          


### -param ArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based index for the array level to address; always use 0 for volume (3D) textures.
          


### -param MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of mipmap levels in the resource.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index which equals MipSlice + (ArraySlice * MipLevels).




## -remarks



A buffer is an unstructured resource and is therefore defined as containing a single subresource. APIs that take buffers do not need a subresource index.
          A texture on the other hand is highly structured. Each texture object may contain one or more subresources depending on the size of the array and the
          number of mipmap levels.
        

For volume (3D) textures, all slices for a given mipmap level are a single subresource index.




## -see-also




<a href="https://msdn.microsoft.com/3acbd433-c28d-4630-aa0e-25f2fb5c32d0">Core Functions</a>



<a href="https://msdn.microsoft.com/865354c5-90cc-4392-a0dc-2d66182f6d05">Resource Functions</a>
 

 

