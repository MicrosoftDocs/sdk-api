---
UID: NF:d3d10effect.ID3D10EffectTechnique.GetPassByIndex
title: ID3D10EffectTechnique::GetPassByIndex (d3d10effect.h)
author: windows-sdk-content
description: Get a pass by index.
old-location: direct3d10\id3d10effecttechnique_getpassbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_getpassbyindex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPassByIndex, GetPassByIndex method [Direct3D 10], GetPassByIndex method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],GetPassByIndex method, ID3D10EffectTechnique.GetPassByIndex, ID3D10EffectTechnique::GetPassByIndex, bf6a09f2-4226-0743-fbab-24f41fc1fd18, d3d10effect/ID3D10EffectTechnique::GetPassByIndex, direct3d10.id3d10effecttechnique_getpassbyindex
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
 - ID3D10EffectTechnique.GetPassByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectTechnique::GetPassByIndex


## -description


Get a pass by index.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass Interface</a>.




## -remarks



A technique contains one or more passes; get a pass using a name or an index.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173708(v=VS.85).aspx">ID3D10EffectTechnique Interface</a>
 

 

