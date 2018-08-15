---
UID: NF:d3d10.ID3D10Device.OMGetBlendState
title: ID3D10Device::OMGetBlendState
author: windows-sdk-content
description: Get the blend state of the output-merger stage.
old-location: direct3d10\id3d10device_omgetblendstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetblendstate.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D10Device interface [Direct3D 10],OMGetBlendState method, ID3D10Device.OMGetBlendState, ID3D10Device::OMGetBlendState, OMGetBlendState, OMGetBlendState method [Direct3D 10], OMGetBlendState method [Direct3D 10],ID3D10Device interface, b8350c99-7325-98c2-8067-e749ec016907, d3d10/ID3D10Device::OMGetBlendState, direct3d10.id3d10device_omgetblendstate
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
 - ID3D10Device.OMGetBlendState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::OMGetBlendState


## -description


Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">blend state</a> of the output-merger stage.


## -parameters




### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173505(v=VS.85).aspx">ID3D10BlendState</a>**</b>

Address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb173505(v=VS.85).aspx">ID3D10BlendState</a>).


### -param BlendFactor




### -param pSampleMask [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb173595(v=VS.85).aspx">sample mask</a>.


#### - BlendFactor[4] [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Array of blend factors, one for each RGBA component.


## -returns



Returns nothing.




## -remarks



The reference count of the returned interface will be incremented by one when the blend state is retrieved. Applications must release returned pointer(s) when they are no longer needed, or else there will be a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

