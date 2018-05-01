---
UID: NF:d3d10.ID3D10Device.OMGetBlendState
title: ID3D10Device::OMGetBlendState method
author: windows-driver-content
description: Get the blend state of the output-merger stage.
old-location: direct3d10\id3d10device_omgetblendstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetblendstate.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D10Device, ID3D10Device interface [Direct3D 10], OMGetBlendState method, ID3D10Device::OMGetBlendState, OMGetBlendState method [Direct3D 10], OMGetBlendState method [Direct3D 10], ID3D10Device interface, OMGetBlendState,ID3D10Device.OMGetBlendState, b8350c99-7325-98c2-8067-e749ec016907, d3d10/ID3D10Device::OMGetBlendState, direct3d10.id3d10device_omgetblendstate
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
-	ID3D10Device.OMGetBlendState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::OMGetBlendState method


## -description


Get the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blend state</a> of the output-merger stage.


## -parameters




### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>**</b>

Address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>).


### -param BlendFactor




### -param pSampleMask [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">sample mask</a>.


#### - BlendFactor[4] [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Array of blend factors, one for each RGBA component.


## -returns



Returns nothing.




## -remarks



The reference count of the returned interface will be incremented by one when the blend state is retrieved. Applications must release returned pointer(s) when they are no longer needed, or else there will be a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

