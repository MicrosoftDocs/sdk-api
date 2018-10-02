---
UID: NF:d3d10.ID3D10Device.VSGetShader
title: ID3D10Device::VSGetShader
author: windows-sdk-content
description: Get the vertex shader currently set on the device.
old-location: direct3d10\id3d10device_vsgetshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vsgetshader.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 1fa1a739-3ba0-3b6b-7587-a11f859e0693, ID3D10Device interface [Direct3D 10],VSGetShader method, ID3D10Device.VSGetShader, ID3D10Device::VSGetShader, VSGetShader, VSGetShader method [Direct3D 10], VSGetShader method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSGetShader, direct3d10.id3d10device_vsgetshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.VSGetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::VSGetShader


## -description


Get the vertex shader currently set on the device.


## -parameters




### -param ppVertexShader [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader</a>**</b>

Address of a pointer to a vertex shader (see <a href="https://msdn.microsoft.com/en-us/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

