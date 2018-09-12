---
UID: NF:d3d10.ID3D10Device.RSGetState
title: ID3D10Device::RSGetState
author: windows-sdk-content
description: Get the rasterizer state from the rasterizer stage of the pipeline.
old-location: direct3d10\id3d10device_rsgetstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rsgetstate.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSGetState method, ID3D10Device.RSGetState, ID3D10Device::RSGetState, RSGetState, RSGetState method [Direct3D 10], RSGetState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSGetState, direct3d10.id3d10device_rsgetstate, e6855c5c-5337-9573-7375-39d3e0d3e83c
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
 - ID3D10Device.RSGetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::RSGetState


## -description


Get the <a href="https://msdn.microsoft.com/en-us/library/Bb172408(v=VS.85).aspx">rasterizer state</a> from the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.


## -parameters




### -param ppRasterizerState [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState</a>**</b>

Address of a pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState</a>) to fill with information from the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

