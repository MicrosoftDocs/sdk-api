---
UID: NF:d3d10.ID3D10Device.PSGetShader
title: ID3D10Device::PSGetShader
author: windows-sdk-content
description: Get the pixel shader currently set on the device.
old-location: direct3d10\id3d10device_psgetshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_psgetshader.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 22e11c1b-a242-803e-3d24-a515820d6e7a, ID3D10Device interface [Direct3D 10],PSGetShader method, ID3D10Device.PSGetShader, ID3D10Device::PSGetShader, PSGetShader, PSGetShader method [Direct3D 10], PSGetShader method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSGetShader, direct3d10.id3d10device_psgetshader
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
 - ID3D10Device.PSGetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.PSGetShader
: 
---

# ID3D10Device::PSGetShader


## -description


Get the pixel shader currently set on the device.


## -parameters




### -param ppPixelShader [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173821(v=VS.85).aspx">ID3D10PixelShader</a>**</b>

Address of a pointer to a pixel shader (see <a href="https://msdn.microsoft.com/en-us/library/Bb173821(v=VS.85).aspx">ID3D10PixelShader</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

