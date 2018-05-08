---
UID: NF:d3d10.ID3D10Device.RSGetState
title: ID3D10Device::RSGetState
author: windows-driver-content
description: Get the rasterizer state from the rasterizer stage of the pipeline.
old-location: direct3d10\id3d10device_rsgetstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rsgetstate.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.RSGetState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::RSGetState


## -description


Get the <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">rasterizer state</a> from the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> of the pipeline.


## -parameters




### -param ppRasterizerState [out]

Type: <b><a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState</a>**</b>

Address of a pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState</a>) to fill with information from the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

