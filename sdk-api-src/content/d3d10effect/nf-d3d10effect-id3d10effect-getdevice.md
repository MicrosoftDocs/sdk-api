---
UID: NF:d3d10effect.ID3D10Effect.GetDevice
title: ID3D10Effect::GetDevice
author: windows-sdk-content
description: Get the device that created the effect.
old-location: direct3d10\id3d10effect_getdevice.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getdevice.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 92eb984e-62b3-6a6f-ab2b-93b561a93fc3, GetDevice, GetDevice method [Direct3D 10], GetDevice method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetDevice method, ID3D10Effect.GetDevice, ID3D10Effect::GetDevice, d3d10effect/ID3D10Effect::GetDevice, direct3d10.id3d10effect_getdevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10effect.h
: 
- ID3D10Effect.GetDevice
: 
---

# ID3D10Effect::GetDevice


## -description


Get the device that created the effect.


## -parameters




### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An effect is created for a specific device, by calling a function such as <a href="https://msdn.microsoft.com/1418857e-bda1-4ffb-bbb9-dfa3709313b1">D3DX10CreateEffectFromFile</a>.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>
 

 

