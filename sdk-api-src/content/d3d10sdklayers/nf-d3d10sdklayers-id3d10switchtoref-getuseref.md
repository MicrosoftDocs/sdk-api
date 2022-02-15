---
UID: NF:d3d10sdklayers.ID3D10SwitchToRef.GetUseRef
title: ID3D10SwitchToRef::GetUseRef (d3d10sdklayers.h)
description: Get a boolean value that indicates the type of device being used.
helpviewer_keywords: ["7b8a132d-2a68-b9bc-338e-0378d33147cd","GetUseRef","GetUseRef method [Direct3D 10]","GetUseRef method [Direct3D 10]","ID3D10SwitchToRef interface","ID3D10SwitchToRef interface [Direct3D 10]","GetUseRef method","ID3D10SwitchToRef.GetUseRef","ID3D10SwitchToRef::GetUseRef","d3d10sdklayers/ID3D10SwitchToRef::GetUseRef","direct3d10.id3d10switchtoref_getuseref"]
old-location: direct3d10\id3d10switchtoref_getuseref.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10switchtoref_getuseref.htm
ms.date: 12/05/2018
ms.keywords: 7b8a132d-2a68-b9bc-338e-0378d33147cd, GetUseRef, GetUseRef method [Direct3D 10], GetUseRef method [Direct3D 10],ID3D10SwitchToRef interface, ID3D10SwitchToRef interface [Direct3D 10],GetUseRef method, ID3D10SwitchToRef.GetUseRef, ID3D10SwitchToRef::GetUseRef, d3d10sdklayers/ID3D10SwitchToRef::GetUseRef, direct3d10.id3d10switchtoref_getuseref
req.header: d3d10sdklayers.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10SwitchToRef::GetUseRef
 - d3d10sdklayers/ID3D10SwitchToRef::GetUseRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10SwitchToRef.GetUseRef
---

# ID3D10SwitchToRef::GetUseRef


## -description

Get a boolean value that indicates the type of device being used.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the device is a software device, <b>FALSE</b> if the device is a hardware device. See remarks.

## -remarks

A hardware device is commonly referred to as a HAL device, which stands for a hardware accelerated device. This means that the pipeline is rendering all of the pipeline commands in hardware, using the GPU. Operating the pipeline with a HAL device gives the best performance generally, but it can be more difficult to debug since resources exist on the GPU instead of the CPU.

A software device implements rendering in software using the CPU with no hardware acceleration. A software device is commonly referred to as a reference device or REF device. Because a REF device implements rendering on the CPU, it is generally slower, but is easier to debug since it allows access to resources.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10switchtoref">ID3D10SwitchToRef Interface</a>
