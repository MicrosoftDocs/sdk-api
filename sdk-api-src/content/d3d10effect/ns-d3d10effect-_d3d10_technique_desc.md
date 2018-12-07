---
UID: NS:d3d10effect._D3D10_TECHNIQUE_DESC
title: "_D3D10_TECHNIQUE_DESC"
author: windows-sdk-content
description: Describes an effect technique.
old-location: direct3d10\d3d10_technique_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_technique_desc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 506d7648-e159-3365-396e-418be67bb2d9, D3D10_TECHNIQUE_DESC, D3D10_TECHNIQUE_DESC structure [Direct3D 10], _D3D10_TECHNIQUE_DESC, d3d10effect/D3D10_TECHNIQUE_DESC, direct3d10.d3d10_technique_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10effect.h
req.include-header: D3D10.h
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
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_TECHNIQUE_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_TECHNIQUE_DESC
req.redist: 
---

# _D3D10_TECHNIQUE_DESC structure


## -description


Describes an effect technique.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that contains the technique name; otherwise <b>NULL</b>.


### -field Passes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of passes in the technique.


### -field Annotations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of annotations.


## -remarks



To get a technique, call <a href="https://msdn.microsoft.com/en-us/library/Bb173712(v=VS.85).aspx">ID3D10EffectTechnique::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205180(v=VS.85).aspx">Effect Structures (Direct3D 10)</a>
 

 

