---
UID: NF:d3d10effect.ID3D10EffectTechnique.GetPassByName
title: ID3D10EffectTechnique::GetPassByName
author: windows-sdk-content
description: Get a pass by name.
old-location: direct3d10\id3d10effecttechnique_getpassbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_getpassbyname.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 35788dc3-3901-8ccb-116d-9dbd8ac5f484, GetPassByName, GetPassByName method [Direct3D 10], GetPassByName method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],GetPassByName method, ID3D10EffectTechnique.GetPassByName, ID3D10EffectTechnique::GetPassByName, d3d10effect/ID3D10EffectTechnique::GetPassByName, direct3d10.id3d10effecttechnique_getpassbyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectTechnique.GetPassByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectTechnique::GetPassByName


## -description


Get a pass by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the pass.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass Interface</a>.




## -remarks



A technique contains one or more passes; get a pass using a name or an index.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173708(v=VS.85).aspx">ID3D10EffectTechnique Interface</a>
 

 

