---
UID: NF:d3d10.D3D10CalcSubresource
title: D3D10CalcSubresource function
author: windows-sdk-content
description: Calculate a subresource index for a texture.
old-location: direct3d10\d3d10calcsubresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10calcsubresource.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 91f92116-0ae9-0407-3cba-2a8ff2762095, D3D10CalcSubresource, D3D10CalcSubresource function [Direct3D 10], d3d10/D3D10CalcSubresource, direct3d10.d3d10calcsubresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CalcSubresource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10CalcSubresource function


## -description


Calculate a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a> index for a texture.


## -parameters




### -param MipSlice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A zero-based index into an array of subtextures; 0 indicates the first, most detailed subtexture (or mipmap level).


### -param ArraySlice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The zero-based index of the first texture to use (in an array of textures).


### -param MipLevels [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of mipmap levels (or subtextures) to use.


## -returns



Type: <b>inline UINT</b>

The index which equals <i>MipSlice</i> + (<i>ArraySlice</i> * <i>MipLevels</i>).




## -remarks



A buffer is an unstructured resource and is therefore defined as containing a single subresource. APIs that take buffers do not need a subresource index. A texture on the other hand is highly structured. Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb694532(v=VS.85).aspx">Resource Functions</a>
 

 

