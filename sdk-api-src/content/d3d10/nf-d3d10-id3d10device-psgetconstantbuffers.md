---
UID: NF:d3d10.ID3D10Device.PSGetConstantBuffers
title: ID3D10Device::PSGetConstantBuffers
author: windows-sdk-content
description: Get the constant buffers used by the pixel shader pipeline stage.
old-location: direct3d10\id3d10device_psgetconstantbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_psgetconstantbuffers.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10Device interface [Direct3D 10],PSGetConstantBuffers method, ID3D10Device.PSGetConstantBuffers, ID3D10Device::PSGetConstantBuffers, PSGetConstantBuffers, PSGetConstantBuffers method [Direct3D 10], PSGetConstantBuffers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSGetConstantBuffers, direct3d10.id3d10device_psgetconstantbuffers, eab94e38-3b29-902e-3cc8-c2e19db2df68
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
 - ID3D10Device.PSGetConstantBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::PSGetConstantBuffers


## -description


Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">pixel shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of buffers to retrieve.


### -param ppConstantBuffers [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

