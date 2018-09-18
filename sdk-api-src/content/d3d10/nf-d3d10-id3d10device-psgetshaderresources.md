---
UID: NF:d3d10.ID3D10Device.PSGetShaderResources
title: ID3D10Device::PSGetShaderResources
author: windows-sdk-content
description: Get the pixel shader resources.
old-location: direct3d10\id3d10device_psgetshaderresources.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_psgetshaderresources.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 54b6aa73-f39a-9734-0be4-f47362f38b2f, ID3D10Device interface [Direct3D 10],PSGetShaderResources method, ID3D10Device.PSGetShaderResources, ID3D10Device::PSGetShaderResources, PSGetShaderResources, PSGetShaderResources method [Direct3D 10], PSGetShaderResources method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSGetShaderResources, direct3d10.id3d10device_psgetshaderresources
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
 - ID3D10Device.PSGetShaderResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::PSGetShaderResources


## -description


Get the pixel shader resources.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from.


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources.


### -param ppShaderResourceViews [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173854(v=VS.85).aspx">ID3D10ShaderResourceView</a>**</b>

Array of <a href="https://msdn.microsoft.com/en-us/library/Bb173854(v=VS.85).aspx">shader resource view</a> interfaces to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

