---
UID: NS:d3d10.D3D10_SUBRESOURCE_DATA
title: D3D10_SUBRESOURCE_DATA
author: windows-sdk-content
description: Specifies data for initializing a subresource.
old-location: direct3d10\d3d10_subresource_data.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_subresource_data.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: D3D10_SUBRESOURCE_DATA, D3D10_SUBRESOURCE_DATA structure [Direct3D 10], d3d10/D3D10_SUBRESOURCE_DATA, direct3d10.d3d10_subresource_data, e1c1f9a8-c810-27f6-5e4c-85302c900510
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D10_SUBRESOURCE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_SUBRESOURCE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_SUBRESOURCE_DATA structure


## -description


Specifies data for initializing a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a>.


## -struct-fields




### -field pSysMem

Type: <b>const void*</b>

Pointer to the initialization data.


### -field SysMemPitch

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The distance (in bytes) from the beginning of one line of a texture to the next line.  
        System-memory pitch is used only for 2D and 3D texture data as it is has no meaning for the other resource types.


### -field SysMemSlicePitch

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The distance (in bytes) from the beginning of one depth level to the next.  
        System-memory-slice pitch is only used for 3D texture data as it has no meaning for the other resource types.


## -remarks



This structure is used in calls to create buffers (<a href="https://msdn.microsoft.com/en-us/library/Bb173544(v=VS.85).aspx">ID3D10Device::CreateBuffer</a>) and textures (<a href="https://msdn.microsoft.com/en-us/library/Bb173559(v=VS.85).aspx">ID3D10Device::CreateTexture1D</a>, 
      <a href="https://msdn.microsoft.com/en-us/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb173561(v=VS.85).aspx">ID3D10Device::CreateTexture3D</a>). 
      If the resource being created does not require a system-memory pitch or a system-memory-pitch slice, then you are free to use those members to 
      pass size information which may help you when debugging a problem creating a resource.

Note that an application should not rely on <b>SysMemPitch</b> being exactly equal to the number of texels in a line times the size of a texel.
      In some cases <b>SysMemPitch</b> will include padding to skip past additional data in a line.  This could be padding for alignment or 
      the texture could be a subsection of a larger texture.  For example the D3D10_SUBRESOURCE_DATA structure could represent a 32 by 32 subsection of a 128 by 128 texture.  
      The value for <b>SysMemSlicePitch</b> will reflect any padding included in <b>SysMemPitch</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

