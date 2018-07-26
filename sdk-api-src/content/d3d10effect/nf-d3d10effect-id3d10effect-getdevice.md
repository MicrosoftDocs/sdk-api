---
UID: NF:d3d10effect.ID3D10Effect.GetDevice
title: ID3D10Effect::GetDevice
author: windows-sdk-content
description: Get the device that created the effect.
old-location: direct3d10\id3d10effect_getdevice.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getdevice.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 92eb984e-62b3-6a6f-ab2b-93b561a93fc3, GetDevice, GetDevice method [Direct3D 10], GetDevice method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetDevice method, ID3D10Effect.GetDevice, ID3D10Effect::GetDevice, d3d10effect/ID3D10Effect::GetDevice, direct3d10.id3d10effect_getdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10Effect.GetDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Effect::GetDevice


## -description


Get the device that created the effect.


## -parameters




### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



An effect is created for a specific device, by calling a function such as <a href="https://msdn.microsoft.com/library/Bb172658(v=VS.85).aspx">D3DX10CreateEffectFromFile</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>
 

 

