---
UID: NF:d3d10.ID3D10Device.RSSetState
title: ID3D10Device::RSSetState
author: windows-sdk-content
description: Set the rasterizer state for the rasterizer stage of the pipeline.
old-location: direct3d10\id3d10device_rssetstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetstate.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSSetState method, ID3D10Device.RSSetState, ID3D10Device::RSSetState, RSSetState, RSSetState method [Direct3D 10], RSSetState method [Direct3D 10],ID3D10Device interface, a9a649fb-abd5-0934-b091-8a577434dfdc, d3d10/ID3D10Device::RSSetState, direct3d10.id3d10device_rssetstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.RSSetState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::RSSetState


## -description


Set the <a href="https://msdn.microsoft.com/en-us/library/Bb172408(v=VS.85).aspx">rasterizer state</a> for the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.


## -parameters




### -param pRasterizerState [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState</a>*</b>

Pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173825(v=VS.85).aspx">ID3D10RasterizerState</a>) to bind to the pipeline.


## -returns



Returns nothing.




## -remarks



To create a rasterizer state interface, call <a href="https://msdn.microsoft.com/en-us/library/Bb173554(v=VS.85).aspx">ID3D10Device::CreateRasterizerState</a>. For more details on setting up the rasterizer state, see <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">Set Rasterizer State</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

